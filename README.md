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

- Problemas con la versión de la API

#### Réplicas 2

- 

#### Autoescala 2 a 4 mediante el uso de CPU al 50%

- ¿Error en la versión de la API?

````bash
error validating data: ValidationError(HorizontalPodAutoscaler.status): missing required field "conditions" in io.k8s.api.autoscaling.v2beta2.HorizontalPodAutoscalerStatus;
````

#### Exponer el servicio cluster ip

-  

#### Utilizar rolling update como estrategia

- 

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

- 

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

- 

#### Setear liveness y readliness

- 

## Iniciar todo

- Ejecutar

````
k create -f actividad-2.yml
````

