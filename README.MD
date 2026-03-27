# 🚀 Sistema de Gestión de Proyectos (DB Design)

¡Hola! Este es el diseño de base de datos que he desarrollado para organizar la información de proyectos y empleados en una empresa. El objetivo principal fue crear una estructura eficiente, evitando la redundancia de datos y asegurando la integridad de la información mediante la **Tercera Forma Normal (3FN)**.

## 🛠️ Sobre el Diseño
Para este modelo, decidí separar las entidades en tres tablas clave. Esto permite que un proyecto tenga muchos empleados y que un empleado pueda participar en varios proyectos sin repetir datos innecesariamente.

### Estructura de Tablas:
1.  **Proyectos:** Contiene el corazón de cada iniciativa (nombre y fechas clave).
2.  **Empleados:** Almacena los datos básicos del equipo de trabajo.
3.  **Asignaciones:** Es nuestra "tabla puente". Aquí es donde ocurre la magia: vinculamos a un empleado con un proyecto y definimos qué rol cumple en él.

## 📐 Diagrama Entidad-Relación (ERD)
El diseño fue realizado en **dbdiagram.io**. Puedes ver la lógica de las relaciones (PK y FK) en la carpeta de documentación o replicarlo con el código DBML incluido.

## 🧠 ¿Por qué es Tercera Forma Normal (3FN)?
He aplicado las reglas de normalización para que la base de datos sea profesional:
* **Adiós a la redundancia:** No repetimos nombres de empleados en la tabla de proyectos.
* **Independencia:** Si un empleado cambia de cargo, solo lo editamos en la tabla `Empleados` y automáticamente se refleja en todas sus participaciones.
* **Atocimidad:** Cada campo guarda un solo dato específico.

## 🚀 Cómo usar este repositorio
1.  **Visualización:** Abre el archivo `diagrama.dbml` en [dbdiagram.io](https://dbdiagram.io/).
2.  **Implementación:** Ejecuta el script SQL en tu motor de base de datos preferido (MySQL, PostgreSQL, etc.).
3.  **Pruebas:** He incluido unos `INSERT` básicos para que puedas ver el sistema en funcionamiento desde el primer segundo.


![Texto alternativo](https://github.com/Kiro061/Reto_DB/blob/main/Captura%20desde%202026-03-27%2007-02-08.png)
