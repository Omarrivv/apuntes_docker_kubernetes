# Guía Docker y Kubernetes - Backend y Frontend

## CREAR PRIMERO LA IMAGEN BACK

### 1. Construir la imagen:
```bash
docker build -t gemirousai .
```

### 2. Etiquetar la imagen para Docker Hub:
```bash
docker tag gemirousai chumpitazkasandra/gemirousai:latest
```

### 3. Subir la imagen a Docker Hub:
```bash
docker login
docker push chumpitazkasandra/gemirousai:latest
```

## Para usar Kubernetes: un Minikube

### 1. Comandos usados paso a paso:

#### Iniciamos un Minikube:
```bash
minikube version
minikube start
```

### 2. Entrar a cd manifest: Aplicar los manifiestos YML
```bash
kubectl apply -f namespace.yml     
kubectl apply -f secret.yml       
kubectl apply -f service.yml     
kubectl apply -f deployment.yml  
```

### 3. Cambiar el Namespace
```bash
kubectl config set-context --current --namespace=kasandra
```

### 4. Verificar el estado de los recursos:
```bash
kubectl get all -n kasandra
kubectl get all,secrets -n kasandra
kubectl get secrets -n kasandra
kubectl config view --minify | grep namespace
```

### 5. Acceder al servicio:
```bash
minikube service microservice-service -n kasandra
```

### 6. Correr en Cluster: 
- **URL:** http://192.168.49.2:30001/api/ai 
```bash
kubectl port-forward service/microservice-service 8090:80 -n kasandra
```

---

## CREACIÓN DE IMAGEN FRONTEND

### Construir imagen en Docker
```bash
docker build -t frongemi .
docker tag frongemi chumpitazkasandra/frongemi:latest
docker images ls
docker logout  # salir
docker login   # iniciar sesión
docker push chumpitazkasandra/frongemi:latest  # subir imagen
docker-compose up   # corre el docker frontend: build: 
docker ps
```

### KUBERNETES
```bash
cd manifest/  # o nombre de la carpeta donde estén YML
kubectl apply -f namespace.yml
kubectl apply -f deployment.yml
kubectl apply -f service.yml
kubectl config set-context --current --namespace=frontend
kubectl get all -n frontend
kubectl get secrets -n frontend
kubectl get deployment -n frontend
kubectl get service -n frontend
```

### Correr el Minikube:
```bash
minikube service microservice-service -n frontend
#        <archivo> <name dentro>         <namespace>
```

### Crear un túnel de puerto la máquina local (host) y el clúster de Kubernetes
```bash
kubectl port-forward service/microservice-service 8090:80 -n frontend
```

---

## COMANDOS DE LIMPIEZA

### Eliminar todos los recursos en el namespace kasandra:
```bash
kubectl delete all --all -n kasandra
```

### Eliminar todos los secrets (si es necesario):
```bash
kubectl delete secrets --all -n kasandra
```

### Eliminar el namespace kasandra:
```bash
kubectl delete namespace kasandra
```

### Eliminar otros recursos específicos (ConfigMaps, PVCs, StatefulSets):
```bash
kubectl delete configmaps --all -n kasandra
kubectl delete pvc --all -n kasandra
kubectl delete statefulsets --all -n kasandra
```

### Verificar que todo se haya eliminado:
```bash
kubectl get all -n kasandra
```

### Eliminar Minikube (si ya no lo necesitas):
```bash
minikube delete
```

---

## CONFIGURACIÓN DE BASE DE DATOS

### Generar string base64:
```bash
echo -n "r2dbc:postgresql://neondb_owner:npg_A8MLQbzEPFe1@ep-summer-art-a4ld12ys-pooler.us-east-1.aws.neon.tech/neondb?" | base64
```

### URLs de conexión:
- **R2DBC:** `r2dbc:postgresql://ep-wild-union-a4ause6j-pooler.us-east-1.aws.neon.tech/neondb?sslmode=require&channel_binding=require`
- **PostgreSQL:** `postgresql://neondb_owner:npg_A8MLQbzEPFe1@ep-summer-art-a4ld12ys-pooler.us-east-1.aws.neon.tech/neondb?sslmode=require&channel_binding=require`

### Credenciales:
- **Username:** `neondb_owner`
- **Password:** `npg_A8MLQbzEPFe1`
- **API Key:** `AIzaSyDh3WS-JXyGBSWEFEP-dK-ee-iAtnSWQHA`

### URL R2DBC completa:
```
r2dbc:postgresql://neondb_owner:npg_A8MLQbzEPFe1@ep-summer-art-a4ld12ys-pooler.us-east-1.aws.neon.tech/neondb?
```
