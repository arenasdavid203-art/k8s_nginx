# k8s-nginx
Proyecto: despliegue sencillo de Nginx en Kubernetes que sirve una página HTML.
# Estructura del proyecto
k8s-nginx/
├── k8s/
│ ├── deployment.yaml # Deployment con réplicas de Nginx
│ ├── service.yaml # Service tipo NodePort
│ └── configmap.yaml # ConfigMap con el contenido HTML
## Requisitos
- kubectl
- minikube (es opcional, recomendado para pruebas locales)

## Despliegue
1. `minikube start` (si usas minikube)
2. `kubectl apply -f k8s/`
3. `minikube service nginx-service` o `kubectl port-forward svc/nginx-service 8080:80`

## Limpieza
`kubectl delete -f k8s/`

## Qué demuestra
- Crear ConfigMap y usarlo como contenido web
- Deployment con réplicas
- Service tipo NodePort
