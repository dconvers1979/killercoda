Crea el archivo replicaset.yml con el siguiente código:

```
apiVersion: apps/v1
kind: ReplicaSet
metadata:
  name: nginx-replicado
  labels:
    app: nginx-ad
spec:
  replicas: 3
  selector:
    matchLabels:
      pod: nginx-server
  template:
    metadata:
      labels:
        pod: nginx-server
    spec:
      containers:
        - name: nginx-server
          image: nginx

```{{copy}}

