# ERS-03 - Subsistemas y Casos de Uso

| Información | Detalle |
|-------------|---------|
| **Responsable** | Nahum Albeño |
| **Rol** | Responsable de Herramientas – Programador |
| **Documento** | ERS-03 – Subsistemas y Casos de Uso |
| **Versión** | 0200 |
| **Fecha** | 29/07/2026 |

---

# 5. Descripción de los Subsistemas

El videojuego **Dead Harvest** se divide en varios subsistemas que permiten organizar las responsabilidades del software y facilitar su desarrollo, mantenimiento y futuras ampliaciones.

Cada subsistema encapsula un conjunto de funcionalidades relacionadas entre sí y se comunica con el resto mediante los componentes principales del motor Unity.

---

## SUB-01 Gameplay Core

Este subsistema contiene las mecánicas principales del videojuego y representa la interacción directa entre el jugador y el entorno.

Sus responsabilidades incluyen:

- Movimiento del jugador en ocho direcciones.
- Sistema de combate cuerpo a cuerpo.
- Cambio de arma mediante las teclas Q y E.
- Administración de vida y estamina.
- Sistema de esquiva (Dash).
- Recolección de botiquines.
- Detección de colisiones entre armas y enemigos.

---

## SUB-02 Inteligencia Artificial

Este subsistema controla el comportamiento de todos los enemigos presentes en la partida.

La Inteligencia Artificial se implementará mediante una **Máquina de Estados Finitos (Finite State Machine)** compuesta por los siguientes estados:

- Patrullar.
- Detectar jugador.
- Perseguir.
- Atacar.
- Regresar al patrullaje.

Cada tipo de enemigo utilizará esta misma estructura, modificando únicamente sus parámetros de velocidad, daño, percepción y comportamiento.

---

## SUB-03 Sistema de Oleadas

Este subsistema será responsable de controlar la progresión de la partida.

Sus funciones principales serán:

- Generar enemigos.
- Controlar la cantidad de enemigos por ronda.
- Incrementar progresivamente la dificultad.
- Administrar el tiempo de descanso entre oleadas.
- Generar el jefe final.

---

## SUB-04 Interfaz de Usuario (UI / UX)

Este subsistema administra todos los elementos gráficos visibles para el jugador.

Incluye:

- HUD.
- Menú Principal.
- Menú de pausa.
- Pantalla de resultados.

Toda la información deberá actualizarse automáticamente durante la partida.

---

## SUB-05 Audio y Efectos

Administra todos los recursos audiovisuales del videojuego.

Incluye:

- Música ambiental.
- Sonidos de combate.
- Sonidos del HUD.
- Efectos de impacto.
- Partículas.
- Sonidos de los enemigos.

---

# 6. Catálogo de Requisitos

## 6.1 Requisitos Generales del Sistema

Los requisitos generales representan las funcionalidades principales que deberá proporcionar el sistema.

| ID | Nombre | Descripción |
|----|---------|-------------|
| RG-01 | Sistema de Combate | El sistema deberá proporcionar un sistema de combate cuerpo a cuerpo utilizando diferentes armas. |
| RG-02 | Sistema de Inteligencia Artificial | El sistema deberá implementar enemigos con comportamientos diferenciados mediante una Máquina de Estados Finitos. |
| RG-03 | Sistema de Oleadas | El sistema deberá controlar la aparición de enemigos y el incremento progresivo de la dificultad. |
| RG-04 | Sistema de Interfaz | El sistema deberá proporcionar una interfaz clara que permita al jugador conocer el estado de la partida. |

---

# 6.2 Casos de Uso

Los casos de uso representan la interacción existente entre los actores y el sistema.

---

## Actores

### ACT-01 Jugador

Corresponde al usuario final del videojuego.

Es responsable de:

- Iniciar partidas.
- Controlar al personaje.
- Combatir enemigos.
- Recoger objetos.
- Completar la partida.

---

### ACT-02 Sistema del Juego

Actor interno encargado de administrar las reglas del videojuego.

Es responsable de:

- Controlar las oleadas.
- Administrar la Inteligencia Artificial.
- Actualizar el HUD.
- Mostrar pantallas.
- Finalizar la partida.

---

# CU-01 Atacar Cuerpo a Cuerpo

**Dependencias**

RG-01

RF-01

---

### Precondiciones

- El jugador se encuentra dentro de una partida.
- Existe un arma equipada.
- El jugador posee estamina suficiente.

---

### Flujo principal

1. El jugador presiona el botón de ataque.
2. El sistema verifica la estamina disponible.
3. Se reproduce la animación correspondiente.
4. Se calcula la colisión entre el arma y los enemigos.
5. El sistema aplica daño.
6. Se reproducen efectos visuales y sonoros.

---

### Postcondiciones

- El enemigo recibe daño.
- La estamina disminuye.
- El estado del enemigo se actualiza.

---

### Excepciones

Si la estamina llega a cero, el ataque continúa siendo posible, pero su velocidad disminuye considerablemente.

---

# CU-02 Cambio de Armamento

**Dependencias**

RG-01

RF-02

---

### Precondiciones

- El jugador posee más de un arma desbloqueada.

---

### Flujo principal

1. El jugador presiona Q o E.
2. El sistema cambia el arma equipada.
3. Se actualizan automáticamente las estadísticas del arma.
4. El HUD refleja el nuevo armamento.

---

### Postcondiciones

El jugador continúa utilizando el nuevo armamento.

---

### Excepciones

Si únicamente existe un arma disponible, el cambio no se realiza.

---

# CU-03 Inteligencia Artificial

**Dependencias**

RG-02

RF-03

---

### Precondiciones

Existe al menos un enemigo activo.

---

### Flujo principal

1. El enemigo patrulla.
2. Detecta al jugador dentro de su radio de percepción.
3. Cambia al estado de persecución.
4. Cuando alcanza la distancia adecuada, comienza el ataque.

---

### Postcondiciones

El enemigo permanece atacando hasta perder al jugador o ser eliminado.

---

### Excepciones

Si el jugador abandona el radio de visión, el enemigo regresa automáticamente al estado de patrullaje.

---

# CU-04 Sistema de Oleadas

**Dependencias**

RG-03

RF-04

---

### Precondiciones

La oleada anterior ha sido completada.

---

### Flujo principal

1. El sistema calcula la siguiente oleada.
2. Se determina la cantidad de enemigos.
3. Se generan los enemigos correspondientes.
4. Comienza la nueva ronda.

---

### Postcondiciones

La dificultad aumenta progresivamente.

---

### Excepciones

Si el jugador pierde toda su vida antes de finalizar la oleada, la partida termina inmediatamente.

---

## Relación entre Casos de Uso y Subsistemas

| Caso de Uso | Subsistema |
|--------------|------------|
| CU-01 | Gameplay Core |
| CU-02 | Gameplay Core |
| CU-03 | Inteligencia Artificial |
| CU-04 | Sistema de Oleadas |

Estos casos de uso constituyen la base para el desarrollo de los Requerimientos Funcionales descritos en la siguiente sección de la ERS y mantienen la trazabilidad con el Product Backlog definido por el equipo.
