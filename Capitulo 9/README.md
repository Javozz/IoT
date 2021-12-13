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

### Filtros basados en el tiempo
<p align="center">
  <img src="https://github.com/Javozz/IoT/blob/main/Capitulo%209/imagenes/time.png" width="950" title="hover text">
</p>

```bash
curl -X GET "localhost:1880/get/timestamp/last/7"
```

<p align="center">
  <img src="https://github.com/Javozz/IoT/blob/main/Capitulo%209/imagenes/last.png" width="950" title="hover text">
</p>

```bash
curl -X GET "localhost:1880/get/timestamp/before/1639359774270/last/5"
```

<p align="center">
  <img src="https://github.com/Javozz/IoT/blob/main/Capitulo%209/imagenes/before.png" width="950" title="hover text">
</p>

```bash
curl -X GET "localhost:1880/get/timestamp/after/1639359774270/last/5"
```

<p align="center">
  <img src="https://github.com/Javozz/IoT/blob/main/Capitulo%209/imagenes/after.png" width="950" title="hover text">
</p>

```bash
curl -X GET "localhost:1880/get/timestamp/during/1639359774270/last/5"
```

<p align="center">
  <img src="https://github.com/Javozz/IoT/blob/main/Capitulo%209/imagenes/during.png" width="950" title="hover text">
</p>

### API de eliminacion de datos

<p align="center">
  <img src="https://github.com/Javozz/IoT/blob/main/Capitulo%209/imagenes/delete.png" width="950" title="hover text">
</p>

```bash
curl -X GET "localhost:1880/get/timestamp/last/5"
```

<p align="center">
  <img src="https://github.com/Javozz/IoT/blob/main/Capitulo%209/imagenes/delete%20time.png" width="950" title="hover text">
</p>

```bash
curl -X GET "localhost:1880/delete/timestamp/id/447"
```

<p align="center">
  <img src="https://github.com/Javozz/IoT/blob/main/Capitulo%209/imagenes/delete%20id.png" width="950" title="hover text">
</p>

El valor del atributo "deleted" cambia a "1" del id:447

<p align="center">
  <img src="https://github.com/Javozz/IoT/blob/main/Capitulo%209/imagenes/delete%20DB.png" width="600" title="hover text">
</p>

```bash
curl -X GET "localhost:1880/get/timestamp/last/5"
```

Al volver mostrar los datos ya no se muestra el id:447

<p align="center">
  <img src="https://github.com/Javozz/IoT/blob/main/Capitulo%209/imagenes/delete%20time%202.png" width="950" title="hover text">
</p>

### Eliminacion completa de los datos
<p align="center">
  <img src="https://github.com/Javozz/IoT/blob/main/Capitulo%209/imagenes/purge.png" width="950" title="hover text">
</p>

```bash
curl -X GET "localhost:1880/purge/timestamp/id/447"
```

<p align="center">
  <img src="https://github.com/Javozz/IoT/blob/main/Capitulo%209/imagenes/purge%20deleted.png" width="950" title="hover text">
</p>

<p align="center">
  <img src="https://github.com/Javozz/IoT/blob/main/Capitulo%209/imagenes/purge%20DB.png" width="600" title="hover text">
</p>
