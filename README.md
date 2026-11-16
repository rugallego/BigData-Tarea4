# UNAD
## Ruben Dario Gallego Tellez
## BigData Tarea 4 - Almacenamiento y Consultas de Datos en Big Data
# Base de datos en MongoDB

Este repositorio contiene el caso de uso: **Catálogo y tasación inteligente de vehículos**.

Para el desarrollo de esta actividad práctica decidí enfocarme en un escenario bastante común en el sector asegurador y automotriz: la consulta y tasación ágil de vehículos a partir de la página web de la Agencia Nacional de Contratación Pública – Colombia Compra Eficiente (https://operaciones.colombiacompra.gov.co/tienda-virtual-del-estado-colombiano/catalogos-iad), de la cual se descargó la base los datos (Catálogo Vehículos 1).

## ¿Cuál es el problema que queremos resolver?

En el día a día, aseguradoras, concesionarios y plataformas de compra y venta necesitan cotizar pólizas o consultar precios comerciales en cuestión de milisegundos. El detalle es que el parque automotor es súper variado: no tiene las mismas características técnicas un automóvil familiar básico que una camioneta 4x4, un chasis de carga pesada o una volqueta.

Si intentamos meter toda esta información en una base de datos relacional tradicional (SQL), nos chocamos contra una pared:
Esquemas amarrados y rígidos: Tendríamos que crear una cantidad exagerada de tablas para conectar las líneas, versiones, tipos de caja y accesorios, o bien crear una tabla gigantesca llena de columnas vacías (campos nulos) porque lo que aplica para un camión no tiene nada que ver con un carro particular.

Consultas lentas: Cada vez que un usuario cotiza un seguro, el sistema tendría que hacer cruces pesados (JOINs) entre múltiples tablas para reconstruir la ficha técnica del carro, lo que en horas pico y con miles de usuarios conectados degrada el rendimiento del servidor.
