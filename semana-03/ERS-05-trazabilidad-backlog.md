# ERS-05 - Trazabilidad y Product Backlog

| Información | Detalle |
|-------------|---------|
| **Responsable** | Gilmar |
| **Rol** | Responsable de Documentación |
| **Documento** | ERS-05 – Trazabilidad y Product Backlog |
| **Versión** | 0200 |
| **Fecha** | 29/07/2026 |
---

# 7. Trazabilidad

La trazabilidad garantiza la relación entre los objetivos del proyecto, los requerimientos del sistema, los casos de uso y las historias de usuario definidas en el Product Backlog.

## 7.1 Matriz de Trazabilidad

| Objetivo | Requerimiento | Caso de Uso | Historia de Usuario |
|----------|---------------|-------------|---------------------|
| OG-01 | RF-01 | CU-01 | HU-02 – Ataque cuerpo a cuerpo |
| OG-01 | RF-02 | CU-02 | HU-07 – Cambio de armas |
| OG-01 | RF-03 | CU-03 | HU-03 – IA básica de zombis |
| OG-01 | RF-04 | CU-04 | HU-04 – Sistema de oleadas |
| OG-01 | RF-05 | — | HU-05 – HUD del jugador |
| OG-01 | RF-06 | — | HU-12 – Menú Principal |
| OG-01 | RF-07 | — | HU-13 – Pantalla de Resultados |
| OG-01 | RF-08 | — | HU-01 – Movimiento del jugador |

---

# 8. Product Backlog

El Product Backlog contiene las historias de usuario priorizadas para el desarrollo del videojuego.

## Sprint 1

| ID | Historia de Usuario | Estado |
|----|---------------------|--------|
| HU-01 | Movimiento del jugador | Sprint 1 |
| HU-02 | Ataque cuerpo a cuerpo | Sprint 1 |
| HU-03 | IA básica de zombis | Sprint 1 |
| HU-04 | Sistema de oleadas | Sprint 1 |
| HU-05 | HUD del jugador | Sprint 1 |

---

## Backlog

| ID | Historia de Usuario | Prioridad |
|----|---------------------|-----------|
| HU-06 | Sistema de mejoras | Media |
| HU-07 | Cambio de armas | Alta |
| HU-08 | Zombis especiales | Alta |
| HU-09 | Jefe final | Alta |
| HU-10 | Incremento de dificultad por oleadas | Alta |
| HU-10b | Balance del juego | Media |
| HU-11 | Visualización del HUD | Media |
| HU-12 | Menú Principal | Alta |
| HU-13 | Pantalla de Resultados | Alta |

---

# 9. Correspondencia entre Requerimientos e Historias de Usuario

| Requerimiento | Historia de Usuario |
|---------------|---------------------|
| RF-01 | HU-02 |
| RF-02 | HU-07 |
| RF-03 | HU-03 |
| RF-04 | HU-04 |
| RF-05 | HU-05 y HU-11 |
| RF-06 | HU-12 |
| RF-07 | HU-13 |
| RF-08 | HU-01 |

---

# 10. Validación de la ERS

Para verificar la consistencia del documento se realizaron las siguientes actividades:

- Revisión de la relación entre objetivos y requerimientos.
- Verificación de la correspondencia entre requerimientos y casos de uso.
- Comprobación de la trazabilidad con las historias de usuario del Product Backlog.
- Comparación con el tablero de GitHub Projects para asegurar la alineación de los elementos documentados.

Como resultado de esta revisión, se confirmó que:

- Los requerimientos funcionales (RF-01 al RF-08) corresponden a las funcionalidades planificadas para el MVP.
- Los requerimientos no funcionales (RNF-01 al RNF-03) establecen criterios mínimos de calidad del sistema.
- Los casos de uso representan las principales interacciones entre el jugador y el videojuego.
- El Product Backlog mantiene coherencia con la planificación del Sprint 1 y las funcionalidades futuras.

---

# 11. Conclusiones

La Especificación de Requisitos de Software define el alcance, comportamiento y restricciones del videojuego **Dead Harvest**, proporcionando una base sólida para las siguientes fases del proyecto.

La documentación establece una relación clara entre los objetivos del proyecto, los requerimientos funcionales y no funcionales, los casos de uso y las historias de usuario, facilitando el desarrollo, seguimiento y validación del sistema.

La versión **0200** incorpora las correcciones realizadas durante la revisión del documento y mantiene la alineación con el repositorio de GitHub y el Product Backlog del equipo **Iron Pixels**.

---

# Control de Versiones

| Versión | Fecha | Descripción |
|----------|------------|-------------|
| 0100 | 27/07/2026 | Primera versión de la ERS. |
| 0200 | 29/07/2026 | Corrección de la clasificación de RF-03 y RF-04, actualización de la trazabilidad y alineación con GitHub Projects. |
