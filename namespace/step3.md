Verificamos la creación del Namespace por medio del siguiente comando:

`kubectl get namespace`{{exec}}

Por defecto los comandos `kubectl get ` realizan las busquedas de objetos en el namespace **default**, luego si queremos realizar la busqueda en un namespace en concreto usamos la bandera -n:

`kubectl get pod -n kube-system`{{exec}}

Y en caso de requerir listar los objetos en todos los namespace disponibles, lo podemos hacer por medio de la bandera -A:

`kubectl get pod -A`{{exec}}
