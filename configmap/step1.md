Crea el archivo configmap.yml con el siguiente código:

```
apiVersion: v1
kind: ConfigMap
metadata:
  name: variables
data:
  URL: "/temp/logs/texto.txt"
  VR_ARGS: "400"
```{{copy}}

Este archivo crea el ConfigMap con dos parámetros.

1. URL
2. VR_ARGS

Para aplicar la confirguración lo hacemos con el siguiente comando:

`kubectl apply -f configmap.yml`{{exec}}

