Crea el archivo probes.yml con el siguiente código:

```
apiVersion: apps/v1
kind: Deployment
metadata:
  name: nginx-probe
  labels:
    app: nginx-probe
    version: v1
spec:
  replicas: 1
  selector:
    matchLabels:
      app: nginx-probe
      version: v1
      pod: nginx
  template:
    metadata:
      labels:
        app: nginx-probe
        version: v1
        pod: nginx
    spec:
      containers:
        - name: nginx
          image: nginx
          startupProbe:
            httpGet:
              path: /index_temporal.html
              port: 80
            periodSeconds: 5
            initialDelaySeconds: 5
            successThreshold: 1
            failureThreshold: 4
          readinessProbe:
            httpGet:
              path: /index_temporal.html
              port: 80
            periodSeconds: 5
            initialDelaySeconds: 5
            successThreshold: 2
            failureThreshold: 4
          livenessProbe:
            httpGet:
              path: /index_temporal.html
              port: 80
```{{copy}}

