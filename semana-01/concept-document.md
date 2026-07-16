# Concept Document — Dead Harvest *(Nombre provisional)*

**Equipo:** Iron Pixels  
**Integrantes:** Cristian Sahon, Marcos Sulugüi, Gilmar Maldonado, Nahum Albeño, Wendy Chumil, Efer Cotúc
**Fecha:** 14-07-2026

---

## 1. Nombre del juego

**Dead Harvest** *(Nombre provisional)*

---

## 2. Género

Acción, Supervivencia y Roguelite 2D con perspectiva **Top-Down (cenital)**.

---

## 3. Sinopsis

Después de una evacuación fallida, el protagonista queda atrapado en una zona de cuarentena completamente infestada. Su única esperanza es abrirse paso entre hordas de zombis, administrar sus recursos y sobrevivir el tiempo suficiente para alcanzar la salida. Para lograrlo deberá adaptarse a enemigos cada vez más peligrosos y aprovechar las mejoras obtenidas durante la partida.

---

## 4. Mecánica principal

El jugador debe sobrevivir a una serie de oleadas de zombis utilizando exclusivamente armas cuerpo a cuerpo. Durante cada ronda deberá administrar su estamina, elegir el arma más adecuada para cada tipo de enemigo y aprovechar el entorno para mantenerse con vida. Al finalizar una oleada podrá seleccionar una mejora temporal que fortalecerá sus habilidades para afrontar el siguiente desafío.

### Loop de juego

- Explorar la arena.
- Combatir enemigos.
- Sobrevivir a la oleada.
- Elegir una mejora.
- Prepararse para la siguiente ronda.
- Derrotar al jefe final.
- Escapar.

---

## 5. Personaje principal

**Nombre:** Ema *(provisional)*

**Descripción visual:**

Un sobreviviente equipado con ropa táctica, mochila y diferentes armas improvisadas para combatir a los infectados.

### Habilidades

- Ataque cuerpo a cuerpo.
- Esquiva (Dash).
- Cambio entre armas.
- Recolección de mejoras y botiquines.

### Controles básicos

- **WASD:** Movimiento.
- **Click izquierdo:** Ataque.
- **Barra espaciadora:** Esquiva.
- **Q / E:** Cambiar de arma.

---

## 6. Pantallas / Niveles

### 1. Menú Principal

Permite iniciar una nueva partida, acceder a las opciones del juego y salir de la aplicación.

### 2. Arena de Supervivencia

Escenario principal donde el jugador enfrenta oleadas de zombis, obtiene mejoras temporales y administra sus recursos mientras la dificultad aumenta progresivamente.

### 3. Batalla Final

Tras superar todas las oleadas aparece un jefe especial con habilidades únicas. El jugador deberá utilizar todo lo aprendido durante la partida para derrotarlo y desbloquear la salida.

### 4. Pantalla Final

Muestra el resultado de la partida (victoria o derrota), estadísticas como tiempo sobrevivido, enemigos eliminados y mejoras obtenidas, además de permitir reiniciar el juego.

---

## 7. Elemento de Inteligencia Artificial

El juego implementará una IA basada en **Máquinas de Estados (Finite State Machine)** para controlar el comportamiento de los enemigos.

Cada tipo de zombi tendrá un comportamiento diferente:

- **Caminante:** Persigue lentamente al jugador.
- **Corredor:** Prioriza alcanzar rápidamente al jugador.
- **Acorazado:** Resiste ataques ligeros y avanza sin detenerse.
- **Explosivo:** Busca acercarse al jugador antes de detonar.

La IA gestionará estados como:

- Patrullar.
- Perseguir.
- Atacar.
- Reaccionar al daño recibido.

Esto permitirá ofrecer diferentes patrones de comportamiento sin recurrir a técnicas avanzadas de aprendizaje automático.

---

## 8. Motor de videojuego

**Unity 2D**

---

## 9. Público objetivo

Jugadores mayores de 13 años que disfrutan juegos de acción, supervivencia y desafíos de corta duración, especialmente quienes buscan partidas rápidas con dificultad progresiva y alta rejugabilidad.

---

## 10. ¿Por qué es viable en 20 semanas?

El proyecto tiene un alcance controlado al desarrollarse principalmente en un único escenario con mecánicas bien definidas. La cantidad de armas, enemigos y mejoras será limitada, permitiendo que un equipo de cuatro estudiantes pueda concentrarse en pulir el sistema de combate, la inteligencia artificial y el balance del juego.

Además, cada partida tendrá una duración aproximada de **15 a 20 minutos**, cumpliendo con el mínimo viable solicitado para el curso.

---

## 11. Riesgos identificados

### Riesgo 1

**Descripción:** El combate puede volverse repetitivo tras varias oleadas.

**Mitigación:** Incorporar distintos tipos de enemigos, armas con estilos de combate diferentes y mejoras temporales que cambien la estrategia del jugador.

---

### Riesgo 2

**Descripción:** La dificultad puede estar desbalanceada, haciendo el juego demasiado fácil o demasiado difícil.

**Mitigación:** Realizar pruebas constantes durante el desarrollo y ajustar parámetros como vida, daño, velocidad de los enemigos y aparición de recursos mediante configuraciones editables.

---

## 12. Retroalimentación recibida en clase

*Pendiente de completar después de la presentación del pitch.*
