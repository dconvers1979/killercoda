Una vez creado el archivo, aplicamos la configuración del archivo por medio del comando kubectl apply

`kubectl apply -f probes.yml`{{exec}}

Esta instrucción creará un Deployment cuyos probes están fallando.

Los probes funcionan, en el caso de http, comprobando una URL que retorne http code entre 200 y antes de 400.

Nginx tiene la página principal en el url **/index.html**

Compriueba que los probes fallan por medio del comando:

`kubectl get pod`{{exec}}

Los Popds deben entrar en **Error**
