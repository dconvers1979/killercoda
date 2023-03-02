Crea el archivo pod.yml con el siguiente código:

```
apiVersion: v1
kind: Pod
metadata:
  name: mi-primerpod
  labels:
    app: nginx
    version: v1
spec:
  containers:
    - name: nginx-server
      image: nginx
```{{copy}}

