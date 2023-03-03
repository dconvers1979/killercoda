**NAMESPACE **

---

El namespace permite generar espacios de trabajo el interior de un cluster de Kubernetes y así organizar objetos que se puedan desplegar en un namespace.

Se puede crear namespaces para separar ambientes (desarrollo, pruebas, produccion), se puede separar por equipos de desarrollo (scrum1, scrum2, scrum3), por clientes o por cuentas.

Los objetos que se pueden desplegar en un namespace son aquellos marcados como **namespaced=true** al ejecutar el siguiente comando:

`kubectl api-resources`{{exec}}
