# LocatorApp Kubernetes Deployment

Este repositorio contiene las configuraciones necesarias para desplegar **LocatorApp** en un entorno **Kubernetes** utilizando **NGINX Ingress**, **Deployments**, **Services**, y **Ingress** para manejar las rutas y las comunicaciones dentro del clúster de Kubernetes.

## Arquitectura

El despliegue de **LocatorApp** está compuesto por los siguientes componentes:

- **Deployment de LocatorApp**: Contiene el contenedor que ejecuta la aplicación **LocatorApp**.
- **Deployment de Route Service**: Servicio auxiliar para manejar rutas dentro de la aplicación.
- **Services**: Define cómo los pods se exponen dentro del clúster.
- **Ingress**: Configura el enrutamiento y la gestión de rutas externas a través de **NGINX Ingress Controller**.

## Requisitos

- **Kubernetes**: Un clúster de Kubernetes en funcionamiento.
- **kubectl**: Herramienta de línea de comandos de Kubernetes configurada.
- **NGINX Ingress Controller**: Necesario para la gestión del enrutamiento de entradas en Kubernetes.

## Descripción de los Archivos

- **`locatorapp-deployment.yaml`**: Contiene la definición del **Deployment** de **LocatorApp**.
- **`route-service-deployment.yaml`**: Contiene la definición del **Deployment** para el servicio que maneja las rutas de la aplicación.
- **`locatorapp-service.yaml`**: Servicio para exponer el contenedor de **LocatorApp**.
- **`route-service.yaml`**: Servicio para exponer el servicio de **Route Service**.
- **`ingress.yaml`**: Configuración del **Ingress** para enrutamiento externo de las rutas `/route` y `/locator`.

## Instrucciones de Despliegue

1. **Clonar el repositorio:**

   ```bash
   git clone https://github.com/Enbebido-ubicate/locatorapp-kubernetes-deployment.git
   cd locatorapp-kubernetes-deployment
