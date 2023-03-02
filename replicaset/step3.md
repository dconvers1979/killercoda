Verificamos la creación del ReplicaSet por medio del siguiente comando:

`kubectl get replicaset`{{exec}}

En la respuesta del comando debe estar el ReplicaSet que creamos con el nombre **nginx-replicado** y debe mostrarnos cuantas réplicas tiene activas.

Para verificar los pods creados podemos ejecutar el comando:

`kubectl get pod`{{exec}}

El cual nos debe mostrar tres réplicas de la plantilla de Pod que especificamos en el yaml de configuración del ReplicaSet.
