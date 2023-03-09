Una vez creado el archivo, aplicamos la configuración del archivo por medio del comando kubectl apply

`kubectl apply -f cronjob.yml`{{exec}}

Esta instrucción creará el CronJob. 

En el caso del ejemplo de este taller, el CronJob se ejecuta cada minuto, creando un Job el cual a su vez crea un Pod asociado a su ejecución.
