# Despliegue de Cognitive Services - Backend y Frontend

## Backend (Rama main)

### 1. Clonar el repositorio backend
```bash
git clone https://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:x-oauth-basic@github.com/vallegrande/CognitiveServices.git --single-branch
cd CognitiveService/manifest
```

### 2. Aplicar manifiestos de Kubernetes
```bash
kubectl apply -f namespace.yml
kubectl apply -f secret.yml
kubectl apply -f service.yml
kubectl apply -f deployment.yml
```

### 3. Configurar contexto y verificar recursos
```bash
kubectl config set-context --current --namespace=ronaldinhoccencho
kubectl get all,secrets
```

### 4. Redirección de puerto para el backend
```bash
kubectl port-forward service/api-cognitive 8090:80
```

### 5. Probar el funcionamiento del backend
```bash
curl http://localhost:8090/api/ai
```

### 6. Verificar servicios
```bash
kubectl get svc -n ronaldinhoccencho
```

## Frontend (Rama develop)

### 1. Clonar el repositorio frontend
```bash
git clone -b develop https://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:x-oauth-basic@github.com/vallegrande/CognitiveServices.git CognitiveFrontend
```

### 2. Aplicar manifiesto del frontend
```bash
cd CognitiveFrotend/k8s
kubectl apply -f frontend-deployment.yaml
```

### 3. Verificar el estado de los pods
```bash
kubectl get all
```
*Esperar que todo esté en estado "Running"*

### 4. Redirección de puerto para el frontend
```bash
kubectl port-forward service/frontend-service 4200:80
```

### 5. Verificar el frontend
```bash
curl http://localhost:4200
```

### 6. Monitorear logs del backend desde el frontend
```bash
kubectl logs -l app=api-cognitive -n ronaldinhoccencho
```

## Configuración Docker

### Dockerfile para el Frontend
```dockerfile
# Etapa 1: build Angular
FROM node:18-alpine AS builder
WORKDIR /app
COPY . .
RUN npm config set registry https://registry.npmjs.org/
RUN npm config set strict-ssl false
RUN npm install
RUN npm run build

# Etapa 2: servir con nginx
FROM nginx:alpine
# ELIMINAR ARCHIVOS POR DEFECTO DE NGINX
RUN rm -rf /usr/share/nginx/html/*
# COPIAR TU APLICACIÓN ANGULAR (dist/.../browser)
COPY --from=builder /app/dist/api_cognitive/browser/ /usr/share/nginx/html/
# CONFIGURACIÓN PERSONALIZADA DE NGINX
COPY nginx.conf /etc/nginx/conf.d/default.conf
EXPOSE 80
```

### Configuración de Nginx
```nginx
server {
  listen 80;
  server_name localhost;
  root /usr/share/nginx/html;
  index index.html;
  location / {
    try_files $uri $uri/ /index.html;
  }
}
```

### ConfigMap para el Frontend
```yaml
apiVersion: v1
kind: ConfigMap
metadata:
  name: frontend-config
  namespace: api-cognitive
data:
  BACKEND_URL: "http://localhost:8090"
  NODE_ENV: "production"
  API_TIMEOUT: "30000"
```

## Notas importantes
- El backend se despliega en el namespace `ronaldinhoccencho`
- El frontend se conecta al backend a través del puerto 8090
- Se requiere que ambos port-forward estén activos para el funcionamiento completo
- Verificar que todos los pods estén en estado "Running" antes de proceder con las pruebas
