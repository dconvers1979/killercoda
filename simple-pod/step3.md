Verificamos la creación del Pod por medio del siguiente comando:

`kubectl get pod`{{exec}}

En la respuesta del comando debe estar el pod que creamos con el nombre **mi-primerpod **y debe estar en estado **Running**

Si queremos verificar la metadata del pod ejecutamos el comando:

`kubectl describe pod mi-primerpod `{{exec}}

De esta forma podemos comprobar los eventos y metadata como los labels, las variables de ambiente, los puertos, y otros detalles.

Para verificar los logs del Pod podemos ejecutar el comando:

`kubectl logs mi-primerpod `{{exec}}

El cual permite visualizar las salidas STDOUT y STDERR del contenedor asociado al pod.
