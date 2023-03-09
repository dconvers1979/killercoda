Verificamos la creación del CronJob por medio del siguiente comando:

`kubectl get cronjob`{{exec}}

Para verificar la ejecución de los Jobs, podemos ejecutar el siguiente comando:

`kubectl get job -w `{{exec}}

Dejamos unos minutos la ejecución del comando para verificar la creación de varios Jobs e interrumpimos la ejecución usando Crtl-c

Por último, podemos verificar los pods creados por medio del comando:

`kubectl get pod `{{exec}}
