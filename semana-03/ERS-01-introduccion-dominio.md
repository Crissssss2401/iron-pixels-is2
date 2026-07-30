# ERS-01 - Introducción y Dominio del Problema

| Información | Detalle |
|-------------|---------|
| **Responsable** | Cristian Sahón |
| **Rol** | Scrum Master – Líder del Equipo |
| **Documento** | ERS-01 – Introducción y Dominio del Problema |
| **Versión** | 0200 |
| **Fecha** | 29/07/2026 |

---

# 1. Introducción
# 1. Introducción

Este documento presenta la **Especificación de Requisitos de Software (ERS)** correspondiente al proyecto **Dead Harvest**, un videojuego de acción y supervivencia en 2D con perspectiva cenital desarrollado como proyecto integrador del curso de Ingeniería de Software II por el equipo **Iron Pixels**.

El propósito de esta especificación es definir de manera clara, organizada y verificable los requerimientos funcionales y no funcionales que servirán como base para el diseño, desarrollo, implementación y validación del videojuego.

La necesidad del proyecto surge como parte del desarrollo del Proyecto Integrador del curso, cuyo objetivo consiste en aplicar metodologías ágiles, Ingeniería de Requisitos, control de versiones mediante GitHub y desarrollo de videojuegos utilizando Unity 2D.

Este documento constituye la referencia principal para el equipo durante todo el ciclo de desarrollo, permitiendo mantener la trazabilidad entre los objetivos del proyecto, los requerimientos, las historias de usuario, los casos de uso y el Product Backlog.

---

## 1.1 Alcance

La primera versión de **Dead Harvest** contempla el desarrollo de un videojuego de supervivencia en 2D con perspectiva cenital, orientado a partidas individuales con una duración aproximada de veinte minutos.

Durante la partida el jugador controlará a un único personaje que deberá sobrevivir a sucesivas oleadas de zombis utilizando exclusivamente armas cuerpo a cuerpo, administrando correctamente recursos como la vida y la estamina mientras enfrenta enemigos con diferentes comportamientos.

La versión MVP incluye las siguientes funcionalidades:

- Movimiento del personaje en ocho direcciones.
- Sistema de combate cuerpo a cuerpo.
- Cuatro armas diferentes (Espada, Hacha, Mazo y Lanza).
- Sistema de cambio de armamento.
- Sistema de estamina.
- Sistema de oleadas progresivas.
- Inteligencia Artificial basada en Máquina de Estados Finitos (FSM).
- Cuatro tipos de enemigos (Caminante, Corredor, Acorazado y Explosivo).
- Sistema de recolección de botiquines.
- HUD con información del jugador.
- Menú principal.
- Pantalla de resultados.
- Jefe final.

Quedan fuera del alcance de esta versión:

- Modo multijugador.
- Guardado persistente de partidas.
- Microtransacciones.
- Personalización de personajes.
- Inteligencia Artificial basada en Machine Learning.
- Generación procedural de niveles.
- Contenido descargable (DLC).

Estas funcionalidades podrán desarrollarse en futuras versiones del videojuego sin afectar el cumplimiento del Producto Mínimo Viable (MVP).

---

## 1.2 Objetivos

### Objetivo General

Desarrollar un videojuego de supervivencia en 2D que ofrezca una experiencia desafiante basada en combate cuerpo a cuerpo, inteligencia artificial y progresión mediante oleadas, aplicando principios de Ingeniería de Software durante todo el proceso de desarrollo.

### Objetivos Específicos

- Desarrollar un MVP completamente funcional y jugable utilizando Unity 2D.
- Implementar un sistema de combate cuerpo a cuerpo con cuatro armas diferenciadas.
- Implementar un sistema de Inteligencia Artificial basado en Máquinas de Estados Finitos para controlar el comportamiento de los enemigos.
- Desarrollar un sistema de oleadas con incremento progresivo de dificultad.
- Diseñar una interfaz clara y responsiva que permita visualizar la información principal del jugador.
- Aplicar buenas prácticas de Ingeniería de Software mediante la elaboración de la ERS, Product Backlog, historias de usuario y trazabilidad entre todos los artefactos del proyecto.
- Obtener un videojuego estable capaz de ejecutarse a 60 FPS en equipos de escritorio con Windows.

---

# 2. Información del Dominio del Problema

## 2.1 Introducción al Dominio del Problema

**Dead Harvest** pertenece al dominio de los videojuegos de acción y supervivencia con perspectiva cenital (Top-Down), donde el jugador debe sobrevivir enfrentando enemigos controlados por Inteligencia Artificial mientras administra recursos limitados.

A diferencia de otros juegos del género, el combate se basa exclusivamente en armas cuerpo a cuerpo, obligando al jugador a mantener un posicionamiento estratégico, administrar correctamente su estamina y seleccionar el arma adecuada según el tipo de enemigo.

El sistema de juego incorpora un modelo de progresión basado en oleadas, incrementando gradualmente la dificultad mediante una mayor cantidad de enemigos y diferentes patrones de comportamiento.

La Inteligencia Artificial de los enemigos será implementada mediante una Máquina de Estados Finitos (Finite State Machine), permitiendo que cada tipo de zombi pueda patrullar, detectar al jugador, perseguirlo y atacarlo según las condiciones del entorno.

El videojuego será desarrollado completamente utilizando Unity 2022.3 LTS y lenguaje de programación C#, utilizando GitHub como sistema de control de versiones y Scrum como metodología de trabajo.

---

## 2.2 Glosario de Términos

| Término | Definición |
|----------|------------|
| Acorazado | Zombi con alta resistencia que reduce parcialmente el daño recibido por armas ligeras. |
| Botiquín | Objeto recolectable que restaura el 25% de la vida del jugador. |
| Caminante | Zombi básico con baja velocidad y comportamiento simple. |
| Corredor | Zombi rápido con poca resistencia física. |
| Dash | Movimiento rápido utilizado para esquivar ataques enemigos consumiendo estamina. |
| Estamina | Recurso utilizado para ejecutar ataques y esquivas. Se recupera automáticamente cuando el jugador permanece inactivo. |
| Explosivo | Zombi que detona al morir causando daño en un área determinada. |
| FSM | Máquina de Estados Finitos utilizada para controlar el comportamiento de la Inteligencia Artificial de los enemigos. |
| Gameplay | Conjunto de mecánicas que conforman la experiencia de juego. |
| Hitbox | Área de colisión utilizada para detectar impactos entre armas y enemigos. |
| HUD | Head-Up Display. Interfaz gráfica que muestra información del jugador durante la partida. |
| Oleada | Ronda de enemigos generada por el sistema con dificultad progresiva. |
| Pooling | Técnica utilizada para reutilizar objetos y optimizar el rendimiento del videojuego. |
| MoSCoW | Técnica de priorización utilizada para clasificar las historias de usuario en Must Have, Should Have, Could Have y Won't Have. |
| RF | Requerimiento Funcional del sistema. |
| RNF | Requerimiento No Funcional del sistema. |

---

**Responsable:** Cristian Sahón  
**Rol:** Scrum Master – Líder del Equipo
