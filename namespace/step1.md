Hay dos formas de crear un namespace, el primero es ejecutando el comando kubectl create:

`kubectl create namespace test`{{exec}}

Aunque esto es posible, si usamos CI/CD o si tenemos versionados los archivos yaml de despliegue es preferible mantenerlo como archivo.

Crea el archivo namespace.yml con el siguiente código:

```
apiVersion: v1
kind: Namespace
metadata:
  name: test2
  labels:
    istio-injection: enabled
```{{copy}}

