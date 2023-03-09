Ahora creamos el archivo del Pod donde vamos a vincular las variables de ambiente, lo llamaremos pod.yml

```
apiVersion: v1
kind: Pod 
metadata:
  name: nginx
spec:
  containers:
    - name: nginx-server
      image: nginx
      env:
        - name: VR_ARGS_FINAL
          valueFrom:
            configMapKeyRef:
              name: variables
              key: VR_ARGS
        - name: URL_FINAL
          valueFrom:
            configMapKeyRef:
              name: variables
              key: URL

```{{copy}}

Una vez creado el archivo, aplicamos la configuración del archivo por medio del comando kubectl apply

`kubectl apply -f pod.yml`{{exec}}

Esta instrucción creará el Pod

Las variables se vinculan por medio del nombre del ConfigMap que creamos anteriormente y la llave que identifica el dato a usar. 
