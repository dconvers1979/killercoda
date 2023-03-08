**SECRET Y VARIABLES DE AMBIENTE **

---

Una de las formas de configurar o personalizar el comportamiento de un Pod es por medio de las variables de ambientes. Las cuales en el Pod se pueden crear en el Dockerfile y sobre escribir al desplegar el Pod.

En algunos casos la información configurable puede ser información sensible, como por ejemplo credenciales de usuarios de base de datos, tokens de acceso entre otros. 

La información sencible en Kubernetes la manejamos por medio de los Secrets.

En este taller revisaremos como usar los secrets para manejar información vinculada a variables de ambiente. 
