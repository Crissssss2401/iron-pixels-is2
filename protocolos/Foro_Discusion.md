# Foro de Discusión – Semana 4
## Ingeniería de Software
### Proyecto: Dead Harvest

**Integrante:** Gilmar Maldonado  
**Rol:** Responsable de Comunicación

---

# Objetivo

Participar en el foro del curso explicando el uso de las relaciones **<<include>>** y **<<extend>>** en diagramas de casos de uso, aplicándolas al proyecto *Dead Harvest*. Además, realizar un comentario constructivo sobre la publicación de otro compañero y documentar la evidencia de participación.

---

# Publicación realizada

## Tema
**Relaciones <<include>> y <<extend>> en Diagramas de Casos de Uso**

Las relaciones **<<include>>** y **<<extend>>** son mecanismos utilizados en los diagramas de casos de uso de UML para representar la interacción entre distintas funcionalidades de un sistema.

La relación **<<include>>** se utiliza cuando un caso de uso necesita ejecutar obligatoriamente otro caso de uso como parte de su funcionamiento. Su propósito es reutilizar procesos comunes y evitar la duplicación de comportamiento entre diferentes funcionalidades.

Por otro lado, la relación **<<extend>>** representa un comportamiento opcional o condicionado. El caso de uso adicional únicamente se ejecuta cuando se cumple una condición específica, sin modificar el flujo principal del caso de uso base.

### Aplicación en Dead Harvest

En el videojuego **Dead Harvest**, un ejemplo de **<<include>>** sería:

**Iniciar partida**
→ **<<include>> Visualizar HUD**

Cada vez que el jugador inicia una partida, el sistema debe mostrar obligatoriamente el HUD con la información principal del juego, como la vida, la estamina, el arma equipada y la oleada actual.

Un ejemplo de **<<extend>>** sería:

**Finalizar partida**
→ **<<extend>> Visualizar resultados**

La pantalla de resultados solamente aparece cuando la partida termina, mostrando información como el resultado obtenido (victoria o derrota), el tiempo sobrevivido, la cantidad de enemigos eliminados, la oleada alcanzada y las mejoras obtenidas durante la partida.

Estas relaciones permiten construir diagramas de casos de uso más claros, organizados y fáciles de mantener, diferenciando las funcionalidades obligatorias de aquellas que solo ocurren bajo determinadas condiciones.

---

## Evidencia de la publicación

> **Agregar aquí la captura de pantalla de la publicación realizada en el foro.**

---

# Comentario realizado a un compañero

Comentario publicado:

> Me pareció muy clara tu explicación sobre la relación **<<include>>**. Como sugerencia, podrías incorporar un ejemplo aplicado al proyecto **Dead Harvest**, ya que facilita comprender cuándo una funcionalidad forma parte obligatoria del flujo principal y cuándo corresponde utilizar una relación **<<extend>>** para representar comportamientos opcionales. Esto hace que el diagrama de casos de uso sea más fácil de interpretar y mantener.

---

## Evidencia del comentario

> **Agregar aquí la captura de pantalla del comentario realizado.**

---

# Enlace al foro

> **Pegar aquí el enlace del foro del curso.**

https://github.com/Crissssss2401/iron-pixels-is2/discussions/26

# Reflexión

La participación en este foro permitió reforzar la comprensión de las relaciones **<<include>>** y **<<extend>>** dentro de los diagramas de casos de uso. Al aplicar estos conceptos al proyecto **Dead Harvest**, fue posible identificar qué funcionalidades forman parte obligatoria del flujo principal del videojuego y cuáles dependen de situaciones específicas durante la partida.

Esta actividad también evidenció la importancia de utilizar correctamente la notación UML para representar de forma clara las interacciones entre el jugador y el sistema, facilitando la comunicación entre los miembros del equipo durante el desarrollo del proyecto mediante la metodología SCRUM.

---

# Conclusión

La actividad permitió fortalecer el análisis de casos de uso y mejorar la capacidad para representar correctamente las funcionalidades del videojuego. Además, la retroalimentación entre compañeros contribuye a mantener una documentación más consistente y alineada con los objetivos del proyecto.
