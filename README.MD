# 🗄️ Sistema de Gestión de Proyectos - Base de Datos

Este repositorio contiene el diseño estructural y el script de creación para una base de datos relacional diseñada para gestionar proyectos y la asignación de colaboradores dentro de una empresa.

## 🎯 Objetivo del Proyecto
El objetivo principal es plantear una arquitectura de datos robusta, escalable y libre de redundancias. El diseño ha sido desarrollado bajo los estándares de la **Tercera Forma Normal (3FN)** para garantizar la integridad de la información.

## 🛠️ Tecnologías Utilizadas
* **Lenguaje:** SQL (DDL - Data Definition Language)
* **Diseño y Modelado:** [dbdiagram.io](https://dbdiagram.io/)

## 📐 Estructura de la Base de Datos

Para resolver la relación de **muchos a muchos** (un proyecto tiene varios empleados y un empleado puede estar en varios proyectos), el sistema se divide en tres tablas esenciales:

1.  **`Proyectos`**: Almacena los datos maestros de cada iniciativa (ID, nombre, fecha de inicio y fin).
2.  **`Empleados`**: Repositorio central de la información del talento humano (ID, nombre, apellido y cargo).
3.  **`Asignaciones`**: Tabla de unión que vincula a los empleados con los proyectos, permitiendo definir el rol específico que desempeña cada persona en una asignación determinada.

## 🧠 Justificación de Normalización (3FN)

El diseño cumple con los criterios de normalización de la siguiente manera:

* **Primera Forma Normal (1FN):** Se garantiza la atomicidad de los datos. No existen campos con múltiples valores (listas) ni grupos repetidos.
* **Segunda Forma Normal (2FN):** Todos los atributos que no forman parte de la clave primaria dependen funcionalmente de la llave completa, eliminando dependencias parciales.
* **Tercera Forma Normal (3FN):** Se han eliminado las dependencias transitivas. Por ejemplo, los datos del empleado (como su cargo) residen únicamente en la tabla `Empleados`, evitando que cambios en el personal obliguen a modificar registros en la tabla de proyectos.

## 🚀 Visualización y Ejecución

### 1. Diagrama Entidad-Relación (ERD)
Puedes visualizar el modelo gráfico utilizando el código DBML adjunto en el editor de [dbdiagram.io](https://dbdiagram.io/).

### 2. Creación del Esquema (SQL)
Para generar la estructura de tablas en un motor de base de datos (MySQL, PostgreSQL, SQL Server):
1.  Copia el contenido del archivo `schema.sql`.
2.  Ejecútalo en tu terminal o gestor de base de datos preferido.
3.  El script creará las tablas y establecerá automáticamente las relaciones de llaves primarias (PK) y foráneas (FK).

---

## 🖼️ Modelo Entidad-Relación
A continuación, se presenta la representación visual de la estructura de la base de datos y sus conexiones:

![Texto alternativo](https://github.com/Kiro061/Reto_DB/blob/main/Captura%20desde%202026-03-27%2007-02-08.png)
