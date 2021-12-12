# CAPITULO 9
## Creacion de una interfaz REST

<p align="center">
  <img src="https://github.com/Javozz/IoT/blob/main/Capitulo%209/imagenes/Flow.png" width="950" title="hover text">
</p>

### Obtener registro de los datos
<p align="center">
  <img src="https://github.com/Javozz/IoT/blob/main/Capitulo%209/imagenes/Obtener%20datos.png" width="950" title="hover text">
</p>

```bash
curl -X GET "localhost:1880/get/topicLike/my*/payloadLike/*/last/5"
```
<p align="center">
  <img src="https://github.com/Javozz/IoT/blob/main/Capitulo%209/imagenes/topicLike1.png" width="950" title="hover text">
</p>

```bash
curl -X GET "localhost:1880/get/topicLike/time*/payloadLike/*/last/5"
```
<p align="center">
  <img src="https://github.com/Javozz/IoT/blob/main/Capitulo%209/imagenes/topicLike2.png" width="950" title="hover text">
</p>

```bash
curl -X GET "localhost:1880/get/topicLike/time*/payloadLike/*88*/last/5"
```
<p align="center">
  <img src="https://github.com/Javozz/IoT/blob/main/Capitulo%209/imagenes/topicLike3.png" width="950" title="hover text">
</p>

### Agregar filtros basados en el tiempo



```bash
curl -X GET "localhost:1880/get/timestamp/last/7"
```

```bash
curl -X GET "localhost:1880/get/mytopic/after//last/5"
```

```bash
curl -X GET "localhost:1880/get/mytopic/during//last/5"
```


