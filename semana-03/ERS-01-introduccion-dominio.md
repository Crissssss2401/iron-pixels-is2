# 01 - Introducción y Dominio del Problema

**Responsable:** Cristian Sahón  
**Rol:** Scrum Master – Líder del Equipo

---

# 1. Introducción

## 1.1 Introducción

Dead Harvest es un videojuego de acción y supervivencia en 2D con perspectiva cenital (Top-Down), desarrollado como proyecto integrador para el curso de Ingeniería de Software II. El objetivo principal del proyecto es diseñar e implementar una experiencia de juego donde el jugador deba sobrevivir a sucesivas oleadas de zombis utilizando exclusivamente armas cuerpo a cuerpo, combinando estrategia, administración de recursos y combate dinámico.

La elaboración de esta Especificación de Requerimientos de Software (ERS) tiene como propósito establecer de forma clara, organizada y verificable todos los requerimientos que servirán como base para el diseño, implementación, pruebas y validación del videojuego. Este documento constituye la referencia principal para el equipo de desarrollo, permitiendo mantener la trazabilidad entre los objetivos del proyecto, los requerimientos funcionales, las historias de usuario y las futuras implementaciones del sistema.

El desarrollo del proyecto busca aplicar los principios de la Ingeniería de Software mediante el uso de metodologías ágiles, gestión de requerimientos y documentación técnica, asegurando que cada funcionalidad implementada responda a una necesidad previamente identificada y validada por el equipo.

---

## 1.2 Alcance

La primera versión de Dead Harvest corresponde al Producto Mínimo Viable (MVP) del videojuego y será desarrollada utilizando Unity 2D como motor principal. El juego estará orientado a partidas individuales con una duración aproximada de entre quince y veinte minutos, en las cuales el jugador deberá sobrevivir a una serie de oleadas de enemigos hasta enfrentarse a un jefe final.

Dentro del alcance de esta versión se contempla la implementación de las mecánicas principales del juego, incluyendo el movimiento del personaje en ocho direcciones, combate cuerpo a cuerpo mediante cuatro armas diferentes, sistema de estamina, recolección de botiquines, inteligencia artificial para distintos tipos de zombis, sistema progresivo de oleadas, interfaz de usuario (HUD), menú principal y pantalla de resultados.

Asimismo, el sistema incorporará diferentes tipos de enemigos con comportamientos específicos controlados mediante una Máquina de Estados Finitos (Finite State Machine), permitiendo ofrecer una experiencia de juego dinámica y desafiante.

Quedan fuera del alcance de esta primera versión funcionalidades como el modo multijugador, guardado persistente de partidas, personalización avanzada del personaje, generación procedural de niveles, inteligencia artificial basada en aprendizaje automático, contenido descargable y cualquier funcionalidad que implique servicios en línea o conexión con servidores externos.

La definición de este alcance responde al objetivo de desarrollar un producto completamente funcional dentro del tiempo establecido para el proyecto, manteniendo un equilibrio entre complejidad técnica, calidad y viabilidad.

---

## 1.3 Objetivos

### Objetivo General

Desarrollar un videojuego de acción y supervivencia en 2D que ofrezca una experiencia desafiante basada en combate cuerpo a cuerpo, inteligencia artificial y progresión por oleadas, aplicando buenas prácticas de Ingeniería de Software durante todo el proceso de desarrollo.

### Objetivos Específicos

- Diseñar un sistema de combate basado exclusivamente en armas cuerpo a cuerpo, permitiendo que cada arma posea características y estrategias diferentes.

- Implementar un sistema de Inteligencia Artificial basado en Máquinas de Estados Finitos que controle el comportamiento de los distintos tipos de enemigos.

- Desarrollar un sistema de oleadas progresivas que incremente gradualmente la dificultad del juego conforme avance la partida.

- Implementar un sistema de administración de recursos basado en vida, estamina y botiquines que obligue al jugador a tomar decisiones estratégicas durante el combate.

- Diseñar una interfaz gráfica clara y minimalista que permita al jugador visualizar en tiempo real su estado durante la partida.

- Aplicar los principios de Ingeniería de Software mediante la elaboración de una ERS, Product Backlog, historias de usuario, trazabilidad de requerimientos y documentación técnica del proyecto.

- Entregar un Producto Mínimo Viable completamente funcional, estable y jugable dentro del tiempo establecido para el curso.

---

# 2. Información del Dominio del Problema

## 2.1 Introducción al Dominio del Problema

Dead Harvest pertenece al género de videojuegos de acción y supervivencia con perspectiva cenital, donde el objetivo principal del jugador consiste en sobrevivir durante el mayor tiempo posible frente a oleadas crecientes de enemigos.

A diferencia de otros juegos del mismo género que basan su mecánica principal en armas de fuego, Dead Harvest centra toda la experiencia de juego en el combate cuerpo a cuerpo. Esto obliga al jugador a administrar correctamente su posición, la estamina disponible, el tipo de arma equipada y el momento adecuado para atacar o esquivar.

El videojuego incorpora una Inteligencia Artificial basada en Máquinas de Estados Finitos (Finite State Machine), permitiendo que los distintos tipos de zombis presenten comportamientos diferenciados durante la partida. De esta forma, la dificultad no depende únicamente del incremento en la cantidad de enemigos, sino también de la variedad de estrategias necesarias para enfrentarlos.

El sistema de progresión está organizado mediante oleadas, donde cada ronda incrementa gradualmente la cantidad y complejidad de los enemigos presentes en la arena. Entre cada oleada el jugador tendrá un breve período de descanso que le permitirá seleccionar mejoras temporales antes de continuar con la siguiente ronda.

El proyecto será desarrollado completamente utilizando Unity 2D y lenguaje de programación C#, empleando herramientas de control de versiones mediante GitHub y una metodología de desarrollo basada en Scrum.

---

## 2.2 Glosario de Términos

| Término | Definición |
|----------|------------|
| Arena | Escenario principal donde se desarrolla la partida. |
| Botiquín | Objeto recolectable que restaura parcialmente la vida del jugador. |
| Caminante | Zombi básico con baja velocidad y comportamiento simple. |
| Corredor | Zombi rápido con poca resistencia pero alta movilidad. |
| Acorazado | Enemigo con alta resistencia que reduce el daño recibido por armas ligeras. |
| Explosivo | Zombi que detona al morir, causando daño en un área determinada. |
| Dash | Movimiento rápido utilizado para esquivar ataques enemigos. |
| Estamina | Recurso utilizado para ejecutar ataques y esquivas. |
| FSM | Máquina de Estados Finitos utilizada para controlar la Inteligencia Artificial de los enemigos. |
| Gameplay | Conjunto de mecánicas que conforman la experiencia de juego. |
| Hitbox | Área de colisión utilizada para detectar impactos entre armas y enemigos. |
| HUD | Interfaz gráfica mostrada durante la partida con información relevante para el jugador. |
| Oleada | Conjunto de enemigos generado durante una ronda del juego. |
| Producto Mínimo Viable (MVP) | Primera versión completamente funcional del videojuego desarrollada durante el proyecto. |
| Unity 2D | Motor de videojuegos utilizado para desarrollar Dead Harvest. |

---
