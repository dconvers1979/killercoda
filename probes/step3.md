Modifica los probes por medio del comando

`kubectl edit deployment nginx-probe`{{exec}}

Una vez logres corregir el archivo, guarda el archivo y Kubernetes actualizará la configuración del Deployment

Comprueba en cualquier momento el estado de los Pods generados por medio del comando:

`kubectl get pod`{{exec}}

Los Pods ahora deben estar en estado **Running**
