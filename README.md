# devops-kubernetes-actividad-1
 Actividad 1 de Kubernetes en Diplomado DevOps Usach.

## Estado general de requerimientos abordados

- Ingress ❌
- Réplicas 2 ✅
- Autoescala 2 a 4 mediante el uso de CPU al 50% ❌
- Exponer el servicio cluster ip ✅
- Utilizar rolling update como estrategia ✅
- Setear variables de ambiente ✅
- Setear variables de ambiente con configmap ✅
- Setear secreto como un archivo✅
- Asignar Volumen de tipo empty ✅
- Setear liveness y readliness ✅

## Detalle de implementación de los requerimientos solicitados

#### Ingress

- Declarado en sección Ingressen yaml
- Problemas con la versión de la API

#### Réplicas 2

- Declarado en archivo yaml

#### Autoescala 2 a 4 mediante el uso de CPU al 50%

- Declarado en sección Autoscaler en yaml
- ¿Error en la versión de la API?

````bash
error validating data: ValidationError(HorizontalPodAutoscaler.status): missing required field "conditions" in io.k8s.api.autoscaling.v2beta2.HorizontalPodAutoscalerStatus;
````

#### Exponer el servicio cluster ip

-  Declarado en sección service en archivo yaml

#### Utilizar rolling update como estrategia

- Declarado en sección deployment archivo yaml

#### Setear variables de ambiente 

- Iniciar sesion ssh en contenedor

```
kubectl exec --stdin --tty nombre-contenedor -- /bin/bash
```

- Probar

````
echo $VARIABLEENYAML
````

#### Setear variables de ambiente con configmap

- Declarado en archivo yaml

#### Setear secreto com un archivo

- Iniciar sesion ssh en contenedor

```bash
kubectl exec --stdin --tty nombre-contenedor -- /bin/bash
```

Revisar archivos con credenciales

````bash
more /etc/secretos/config.yaml
````

#### Asignar Volumen de tipo empty

- Declarado en sección deployment en archivo yaml

#### Setear liveness y readliness

- Declarado en sección deployment en archivo yaml

## Iniciar todo

- Ejecutar

````
k create -f actividad-1.yml
````

