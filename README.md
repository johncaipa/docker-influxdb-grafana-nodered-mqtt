# docker-influxdb-grafana-nodered-mqtt

Un script docker-compose que incluye influxdb, grafana, nodered y mqtt solo con fines de prueba y enseñanza.

## Configuración e inicio de contenedores

Una vez clonado el repositorio en su máquina virtual Ubuntu, ejecute el siguiente comando para descargar las imagenes y levantar los contenedores.

```bash
docker-compose up -d
```

## Acceder a las aplicaciones

NOTA: antes de poder acceder a las aplicaciones necesita abrir los puertos en VirtualBox.
Para aceder a Node-RED en su buscador web ingrese la siguiente URL:
http://localhost:1880/

## Configuration

### Configuración de InfluxDB

La configuración se puede realizar con el archivo influxdb.env (opcional).
Para aceder a InfluxDB en su buscador web ingrese la siguiente URL:
http://localhost:8086/
Al acceder le pedirá crear lo siguiente: Organization, Bucket y Measurement, asi mismo debe crear un API Token para poder usarlo en Node-RED y Grafana.

### Configuración de Grafana

La configuración se realiza en el archivo grafana.env (opcional).
Para aceder a Grafana en su buscador web ingrese la siguiente URL:
http://localhost:3000/
Para conectar Grfana a la base de datos influxdb, se puede usar el nombre de host 'influxdb': http://influxdb:8086 y el API Token creado anteriormente.

## Detención de los contenedores

Una vez terminada la práctica deberá detener los contenedores en su máquina virtual, utilice el siguiente comando para esto.

```bash
docker-compose down
```
