
id: identificador-unico-del-codelab
title: Bases de Datos No-SQL Orientadas a Columnas
summary: El Codelab guiará a los usuarios a través de la comprensión fundamental de las bases de datos No-SQL orientadas a columnas, sus características distintivas, aplicaciones prácticas, pros y contras, y ejemplos concretos.
author: Tu Nombre
categories: codelab,markdown
environments: Web
status: Published
feedback link: https://github.com/tu_usuario/tu_repo/issues
analytics account: UA-XXXXXX-X

# NO-SQL Orientado a Columnas

## ¿Qué es "Orientado a Columnas"?
Duration: 0:03:00 

### Cajas de información
Texto plano.

### Añade una imagen
¡Añadiendo una imagen!

![Descripción de la imagen](assets/prueba.png)


### Lista con viñetas
Texto plano en una lista con viñetas:

* Hola
* CodeLab
* Mundo

¡Ya tienes tu lista con viñetas creada!

### Lista numerada
1. Lista
2. Utilizando
3. Números

¡Ya tienes tu lista numerada creada!

## Apache Casandra
Duration: 0:05:00

Apache Cassandra es un sistema de gestión de bases de datos **NoSQL** distribuido y altamente escalable, diseñado para manejar grandes volúmenes de datos en múltiples servidores sin un único punto de fallo.​ Es ideal para aplicaciones que requieren características como: **Alta disponibilidad**, **Alta velocidad de escritura** y **lectura, Escalabilidad horizontal** (puedes añadir más columnas fácilmente).

### Historia de Apache Cassandra

* En 2007 **Facebook** crea Cassandra para gestionar el motor de búsqueda de mensajes (**Inbox Search**), combinando lo mejor de **Amazon Dynamo** (**alta disponibilidad**) y Google Bigtable (**modelo de datos flexible**).
* En 2008 **Facebook** libera **Cassandra** como código abierto.
* En 2009 **Cassandra** se convierte en un proyecto de **Apache Incubator**. Poco después, se vuelve un proyecto de nivel superior dentro de la **Apache Software Foundation**.
* En 2010 Empresas como **Twitter**, **Netflix**, **eBay** y **Apple** comienzan a usar **Cassandra** para aplicaciones críticas.
* En 2020 – 2024 Se lanzan versiones más estables como 3.x, 4.x, con mejoras en rendimiento, seguridad y facilidad de operación.
* En la actualidad **Cassandra** es una de las bases de datos **NoSQL** más utilizadas en sistemas distribuidos, con una comunidad activa y soporte empresarial.

### DDL de Apache Cassandra
| Comando DDL | Descripción                                      | Ejemplo                                                                                                                               |
|-------------|----------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| CREATE KEYSPACE | Crea un nuevo keyspace (una base lógica para las tablas)​       | `CREATE KEYSPACE tienda WITH replication = {'class': 'SimpleStrategy', 'replication_factor': 3};​`                                  |
| DROP KEYSPACE   | Elimina un KEYSPACE.                 | `DROP KEYSPACE tienda;`                                                                                                             |
| CREATE TABLE  | Crea una nueva tabla con claves primarias definidas​      | `CREATE TABLE productos (id UUID PRIMARY KEY, nombre TEXT, precio DECIMAL);​`                                                                            |
| ALTER TABLE   | Modifica una tabla existente (añadir columnas, por ejemplo)​. | `ALTER TABLE productos ADD stock INT;`                                                                                   |
| DROP TABLE    | Elimina una tabla​                             | `DROP TABLE productos;​`                                                                                                                  |
| USE           | Selecciona el keyspace activo.                          | `USE tienda;`                                                                                                                          |

### DML de Apache Cassandra
| Comando CQL | Descripción en Español                | Ejemplo                                                                 |
|-------------|---------------------------------------|-------------------------------------------------------------------------|
| INSERT      | Agrega nuevas filas o registros a las tablas | `INSERT INTO productos (id, nombre, precio, stock) VALUES (uuid(), 'Laptop', 3500.00, 20);` |
| SELECT      | Consulta datos​ | `SELECT * FROM productos;​`                     |
| UPDATE      | Modifica valores de una fila existente​. | `UPDATE productos SET stock = 15 WHERE id = ...;`   |
| DELETE      | Elimina una fila o columna espécifica​      | `DELETE FROM productos WHERE id = ...;​`                                  |

### Instalacion de Apache Cassandra
### JAVA11
* Es necesario que se instale java 11 para poder usar cassandra​
### Variables de entorno​
* Es necesario configurar java como variable de entorno para poder iniciarlizar cassandra​
### Otros lenguajes​
* En necesario el lenguaje de programacion con le que se interactuará con la base de datos​

### Ejemplo en Apache Cassandra
### Codificacion.
![Descripción de la imagen](assets/CodeEjemploCassandra.png)
### Salida en Cassandra DB
![Descripción de la imagen](assets/SalidaEjemploCassandra.png)

## Microsoft Azure Cosmos DB
Duration: 0:03:00

### Cajas de información
Texto plano.

### Lista con viñetas
Texto plano en una lista con viñetas:

* Hola
* CodeLab
* Mundo

¡Ya tienes tu lista con viñetas creada!

### Lista numerada
1. Lista
2. Utilizando
3. Números

¡Ya tienes tu lista numerada creada!

## APACHE HBASE
Duration: 0:03:00

### Cajas de información
Texto plano.

### Lista con viñetas
Texto plano en una lista con viñetas:

* Hola
* CodeLab
* Mundo

¡Ya tienes tu lista con viñetas creada!

### Lista numerada
1. Lista
2. Utilizando
3. Números

¡Ya tienes tu lista numerada creada!

## DataStax Enterprise 
Duration: 0:03:00

### Cajas de información
Texto plano.

### Lista con viñetas
Texto plano en una lista con viñetas:

* Hola
* CodeLab
* Mundo

¡Ya tienes tu lista con viñetas creada!

### Lista numerada
1. Lista
2. Utilizando
3. Números

¡Ya tienes tu lista numerada creada!

## ScyllaDB 
Duration: 0:03:00

### ¿La base de datos más rápida?

**ScyllaDB** es una base de datos NoSQL distribuida, de código abierto, diseñada desde cero en **C++** para aprovechar al máximo el hardware moderno. Es una alternativa compatible con Apache Cassandra pero con un rendimiento superior.

---

### Características Clave

* **Lenguaje de Programación:** Escrita en **C++**, a diferencia de otras como MongoDB que usan Java.
* **Compatibilidad:** Soporta **CQL** (Cassandra Query Language) y utiliza formatos **SSTable**.
* **Modelo de Datos:** Almacenamiento en **columnas**, similar a MySQL. No basado en documentos como MongoDB.
* **Motor Alternativo a Cassandra:** Reescrito completamente para mejorar eficiencia.

---

### ¿Por qué ScyllaDB es más rápida?

* **Lenguaje de Bajo Nivel (C++):** Menor sobrecarga comparado con Java.
* **Seastar:** Biblioteca asincrónica que permite operaciones no bloqueantes.
  1. Menor latencia.
  2. Mayor rendimiento.
* **Optimización del Hardware:** 
  1. Exprime al máximo las capacidades del servidor moderno.

---

### Adopción y Casos de uso
* **Discord:** Plataforma de comunicación masiva.
![Discord](assets/Discord.png)
* **Samsung:** Diversas aplicaciones empresariales.
![Samsung](assets/Samsung.png)
* **AppsFlyer:** Análisis de marketing.
![AppsFlyer](assets/AppsFlyer.png)
* **Zillow:** Mercado inmobiliario digital.
![Zillow](assets/Zillow.png)
* **Outbrain:** Descubrimiento de contenido.
![Outbrain](assets/Outbrain.png)
* Y muchas más empresas con alta demanda de rendimiento.

---

### Comandos DDL en ScyllaDB
Comandos más comúnes para definir y administrar la estructura de la base de datos.
| Comando CQL | Descripción                                      | Ejemplo                                                                                                                               |
|-------------|----------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| CREATE KEYSPACE | Crea un nuevo espacio de nombres (base de datos).       | `CREATE KEYSPACE mitienda WITH replication = {'class': 'SimpleStrategy', 'replication_factor': 1};`                                  |
| DROP KEYSPACE   | Elimina un espacio de nombres existente.                 | `DROP KEYSPACE mitienda;`                                                                                                             |
| CREATE TABLE  | Crea una nueva tabla dentro del keyspace activo.      | `CREATE TABLE usuarios (id UUID PRIMARY KEY, nombre TEXT);`                                                                            |
| ALTER TABLE   | Modifica la estructura de una tabla (añadir/eliminar columnas). | `ALTER TABLE usuarios ADD COLUMN email TEXT;`                                                                                   |
| DROP TABLE    | Elimina una tabla existente.                             | `DROP TABLE usuarios;`                                                                                                                  |
| USE           | Selecciona el keyspace activo.                          | `USE mi_app;`                                                                                                                          |

---

### Comandos DML en ScyllaDB
Comandos para trabajar con los datos dentro de las tablas.

| Comando CQL | Descripción en Español                | Ejemplo                                                                 |
|-------------|---------------------------------------|-------------------------------------------------------------------------|
| INSERT      | Agrega nuevos registros a las tablas. | `INSERT INTO usuarios (id, nombre, email) VALUES (uuid(), 'Ana', 'ana@email.com');` |
| SELECT      | Recupera datos de una o más tablas. | `SELECT nombre, email FROM usuarios WHERE id = ...;`                     |
| UPDATE      | Modifica registros existentes en una tabla. | `UPDATE usuarios SET email = 'ana.nueva@email.com' WHERE id = ...;`   |
| DELETE      | Elimina registros de una tabla.      | `DELETE FROM usuarios WHERE id = ...;`                                  |


---

### Problemas Comunes en la Instalación

* **Sistema:** Necesidad de Linux moderno con suficiente RAM y espacio en disco.
* **Red:** Puertos bloqueados o IPs mal configuradas.
* **Dependencias:** Paquetes faltantes o mal instalados.
* **`scylla.yaml`:** Archivo de configuración principal mal escrito.
* **Permisos:** Problemas de acceso a carpetas o archivos.
* **Conflictos de Puertos:** Otros servicios usando los mismos puertos.

---
### Compatibilidad

* **Optimizado para Linux:** Especialmente Ubuntu.
* **Windows:** Recomendado usar **Docker** para ejecutarlo.

---

### Demostración Práctica

#### 1. Crear configuración de Docker Compose

```yaml
version: '3'
services:
  scylla-node1:
    image: scylladb/scylla
    ports:
      - "9042:9042"
    volumes:
      - scylla-data1:/var/lib/scylla
    command: --seeds=scylla-node1

volumes:
  scylla-data1:
```
#### 2. Crear estructura de datos

```sql
CREATE KEYSPACE tienda WITH replication = {
  'class': 'SimpleStrategy',
  'replication_factor': 1
};
USE tienda;

CREATE TABLE productos (
  id UUID PRIMARY KEY,
  nombre TEXT,
  precio DECIMAL,
  stock INT,
  categoria TEXT
);

CREATE INDEX idx_categoria ON productos (categoria);
```

#### 3. Operaciones básicas con datos

```sql
-- Insertar producto
INSERT INTO productos (id, nombre, precio, stock, categoria)
VALUES (uuid(), 'Laptop Pro', 1299.99, 50, 'Electrónicos');

-- Consultar productos
SELECT * FROM productos;

-- Filtrar por categoría
SELECT * FROM productos WHERE categoria = 'Electrónicos';

-- Actualizar stock
UPDATE productos SET stock = stock - 1 WHERE id = [ID_PRODUCTO];

-- Eliminar producto
DELETE FROM productos WHERE id = [ID_PRODUCTO];
```

#### 4. Rendimiento y monitoreo

```sql
-- Activar rastreo para analizar rendimiento
TRACING ON;
SELECT * FROM productos WHERE categoria = 'Electrónicos';
TRACING OFF;

-- Ver estado del sistema
DESCRIBE KEYSPACES;
DESCRIBE TABLES;

-- Estadísticas del sistema
nodetool status
nodetool tablestats tienda.productos
```

## Google Cloud
Duration: 0:03:00

### Cajas de información
Texto plano.

### Lista con viñetas
Texto plano en una lista con viñetas:

* Hola
* CodeLab
* Mundo

¡Ya tienes tu lista con viñetas creada!

### Lista numerada
1. Lista
2. Utilizando
3. Números

¡Ya tienes tu lista numerada creada!


## Microsoft Azure
Duration: 0:03:00

### Cajas de información
Texto plano.

### Lista con viñetas
Texto plano en una lista con viñetas:

* Hola
* CodeLab
* Mundo

¡Ya tienes tu lista con viñetas creada!

### Lista numerada
1. Lista
2. Utilizando
3. Números

¡Ya tienes tu lista numerada creada!


## IBM Db2
Duration: 0:03:00

### Cajas de información
Texto plano.

### Lista con viñetas
Texto plano en una lista con viñetas:

* Hola
* CodeLab
* Mundo

¡Ya tienes tu lista con viñetas creada!

### Lista numerada
1. Lista
2. Utilizando
3. Números

¡Ya tienes tu lista numerada creada!