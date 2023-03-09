Ahora creamos el archivo del Pod donde vamos a vincular las variables de ambiente, lo llamaremos pod.yml

```
apiVersion: v1
kind: Pod
metadata:
  name: mysql-server
  labels:
    app: secret-app
spec:
  containers:
    - name: mysql
      image: mysql
      env:
        - name: MYSQL_ROOT_PASSWORD
          valueFrom:
            secretKeyRef:
              name: credenciales-mysql
              key: DB_ROOT_PASSWORD
        - name: MYSQL_USER
          valueFrom:
            secretKeyRef:
              name: credenciales-mysql
              key: DB_USER
        - name: MYSQL_PASSWORD
          valueFrom:
            secretKeyRef:
              name: credenciales-mysql
              key: DB_PASSWORD

```{{copy}}

Una vez creado el archivo, aplicamos la configuración del archivo por medio del comando kubectl apply

`kubectl apply -f pod.yml`{{exec}}

Esta instrucción creará el Pod

Las variables se vinculan por medio del nombre del secret que creamos anteriormente y la llave que identifica el dato a usar. 
