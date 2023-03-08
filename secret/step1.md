Crea el archivo secret.yml con el siguiente código:

```
apiVersion: v1
kind: Secret
metadata:
  name: credenciales-mysql
  labels:
    app: secret-app
type: Opaque
data:
  DB_USER: YWRtaW5pc3RyYWRvcg==
  DB_PASSWORD: cGFzc3dvcmQ=
  DB_ROOT_PASSWORD: cGFzc3dvcmQ=

```{{copy}}

Este archivo crea el secret con tres parámetros.

1. DB_USER
2. DB_PASSWORD
3. DB_ROOT_PASSWORD

Los valores que toman las variables se codifican Base64.

Para aplicar la confirguración lo hacemos con el siguiente comando:

`kubectl apply -f secret.yml`{{exec}}

