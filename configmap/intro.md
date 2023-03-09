**CONFIGMAPS Y VARIABLES DE AMBIENTE **

---

Una de las formas de configurar o personalizar el comportamiento de un Pod es por medio de las variables de ambientes. Las cuales en el Pod se pueden crear en el Dockerfile y sobre escribir al desplegar el Pod.

Cuando la información que se quiere manejar como variables de ambientes no es información sensible, podemos manejarla por medio de un ConfigMap. 

El uso del ConfigMap nos permite centralizar configuraciones entre diferentes Pods, de esta manera podemos controlar facinmente la configuración de nuestras aplicaciones en Kubernetes.


En este taller revisaremos como usar los ConfigMaps para manejar información vinculada a variables de ambiente. 
