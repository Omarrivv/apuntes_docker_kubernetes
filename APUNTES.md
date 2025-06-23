# Proyecto Kubernetes - API CRUD de Productos

## 📁 Estructura del Proyecto

```
kubernetes-python-crud/
├── app/
│   ├── app.py                 # API Flask principal
│   └── requirements.txt       # Dependencias Python
├── docker/
│   └── Dockerfile            # Imagen de la aplicación
├── kubernetes/
│   ├── namespace.yaml        # Namespace del proyecto
│   ├── deployment.yaml       # Deployment de la API
│   ├── service.yaml          # Service para exponer la API
│   ├── hpa.yaml             # Horizontal Pod Autoscaler
│   └── ingress.yaml         # Ingress para acceso externo
├── scripts/
│   ├── build.sh             # Script para construir imagen
│   ├── deploy.sh            # Script para desplegar
│   └── test-api.sh          # Script para probar la API
└── README.md                # Documentación

```

## 🎯 Objetivos de Aprendizaje

### 1. **Conceptos Básicos de Kubernetes**
- **Pods**: Unidad más pequeña de despliegue
- **Deployments**: Gestión de replicas y actualizaciones
- **Services**: Exposición de aplicaciones
- **Namespaces**: Organización de recursos

### 2. **Componentes del Control Plane**
- **API Server**: Punto de entrada para todas las operaciones
- **etcd**: Base de datos distribuida del cluster
- **Scheduler**: Asigna pods a nodos
- **Controller Manager**: Gestiona el estado deseado

### 3. **Componentes de los Nodos**
- **kubelet**: Agente que ejecuta en cada nodo
- **kube-proxy**: Maneja el networking
- **Container Runtime**: Docker/containerd

## 🚀 Plan de Aprendizaje Paso a Paso

### Fase 1: Preparación (Días 1-2)
1. **Instalar herramientas**:
   - Docker Desktop
   - kubectl
   - Minikube o kind
   - Visual Studio Code con extensiones de Kubernetes

2. **Conceptos fundamentales**:
   - Contenedores vs Pods
   - Imágenes de Docker
   - YAML básico

### Fase 2: Desarrollo de la API (Días 3-4)
1. **Crear la aplicación Flask**
2. **Containerizar con Docker**
3. **Probar localmente**

### Fase 3: Kubernetes Básico (Días 5-7)
1. **Deployments**: Desplegar la aplicación
2. **Services**: Exponer la aplicación
3. **ConfigMaps y Secrets**: Configuración
4. **Persistent Volumes**: Almacenamiento

### Fase 4: Escalabilidad y Monitoreo (Días 8-10)
1. **Horizontal Pod Autoscaler**: Escalado automático
2. **Resource Limits**: Gestión de recursos
3. **Health Checks**: Liveness y Readiness probes
4. **Ingress**: Acceso desde el exterior

## 🛠️ Comandos Kubernetes Esenciales

### Gestión de Cluster
```bash
# Ver información del cluster
kubectl cluster-info

# Ver nodos
kubectl get nodes

# Ver todos los recursos
kubectl get all
```

### Gestión de Pods
```bash
# Ver pods
kubectl get pods

# Describir un pod
kubectl describe pod <pod-name>

# Logs de un pod
kubectl logs <pod-name>

# Ejecutar comando en un pod
kubectl exec -it <pod-name> -- /bin/bash
```

### Gestión de Deployments
```bash
# Crear deployment
kubectl apply -f deployment.yaml

# Ver deployments
kubectl get deployments

# Escalar deployment
kubectl scale deployment <name> --replicas=5

# Actualizar imagen
kubectl set image deployment/<name> container=<new-image>
```

## 📊 Métricas y Monitoreo

### Recursos que aprenderás a monitorear:
- **CPU y Memoria**: Uso de recursos por pod
- **Requests vs Limits**: Gestión de recursos
- **Replicas**: Estado de escalado
- **Health Status**: Estado de salud de la aplicación

## 🔧 Troubleshooting Común

### Problemas frecuentes y soluciones:
1. **Pods en estado Pending**: Recursos insuficientes
2. **ImagePullBackOff**: Imagen no encontrada
3. **CrashLoopBackOff**: Aplicación falla al iniciar
4. **Service no accesible**: Configuración de networking

## 📚 Recursos Adicionales

### Documentación Oficial:
- [Kubernetes Docs](https://kubernetes.io/docs/)
- [Docker Docs](https://docs.docker.com/)

### Cursos Recomendados:
- Certified Kubernetes Administrator (CKA)
- Kubernetes for Developers (CKAD)

### Herramientas Útiles:
- **k9s**: Terminal UI para Kubernetes
- **Helm**: Gestor de paquetes
- **Lens**: IDE para Kubernetes
- **kubectl-tree**: Visualizar recursos relacionados

## 🎓 Certificaciones

Una vez domines estos conceptos, puedes prepararte para:
- **CKAD**: Certified Kubernetes Application Developer
- **CKA**: Certified Kubernetes Administrator
- **CKS**: Certified Kubernetes Security Specialist
