# ERS-04 - Requerimientos del Sistema

| Información | Detalle |
|-------------|---------|
| **Responsable** | Wendy |
| **Rol** | Responsable de Diseño y Experiencia de Usuario (UI/UX) |
| **Documento** | ERS-04 – Requerimientos del Sistema |
| **Versión** | 0200 |
| **Fecha** | 29/07/2026 |

---

# 6.3 Requisitos del Sistema

Los siguientes requerimientos describen el comportamiento que deberá implementar el videojuego **Dead Harvest**. Cada requerimiento mantiene trazabilidad con los Requisitos Generales (RG), Casos de Uso (CU) y las Historias de Usuario (HU) definidas por el equipo.

---

# 6.3.1 Requisitos Funcionales

## RF-01 – Ataque cuerpo a cuerpo

**Dependencias:** RG-01, CU-01

### Requerimiento de Usuario

Como jugador, quiero atacar utilizando armas cuerpo a cuerpo para eliminar zombis y defenderme durante la partida.

### Requerimientos del Sistema

- El sistema deberá ejecutar la animación correspondiente al arma equipada cuando el jugador presione el botón de ataque.
- El sistema deberá calcular la colisión entre el arma y los enemigos.
- El sistema deberá aplicar el daño correspondiente al arma utilizada.
- El sistema deberá reproducir efectos visuales y sonoros al conectar un ataque.

---

## RF-02 – Cambio de armamento

**Dependencias:** RG-01, CU-02

### Requerimiento de Usuario

Como jugador, quiero cambiar entre distintas armas para utilizar la más adecuada según el tipo de enemigo.

### Requerimientos del Sistema

- El sistema permitirá cambiar de arma mediante las teclas Q y E.
- El cambio deberá reflejarse inmediatamente en el daño, alcance, velocidad y animaciones.
- El sistema deberá mantener disponibles las armas Espada, Hacha, Mazo y Lanza.

---

## RF-03 – Inteligencia Artificial de los enemigos

**Dependencias:** RG-02, CU-03

### Requerimiento de Usuario

Como jugador, quiero que los zombis reaccionen de forma inteligente para mantener una sensación constante de peligro.

### Requerimientos del Sistema

- El sistema implementará una Máquina de Estados Finitos (FSM).
- Los estados serán Patrullar, Perseguir y Atacar.
- El enemigo cambiará automáticamente de estado según la posición del jugador.

---

## RF-04 – Sistema de Oleadas

**Dependencias:** RG-03, CU-04

### Requerimiento de Usuario

Como jugador, quiero enfrentar oleadas cada vez más difíciles para mantener el reto durante toda la partida.

### Requerimientos del Sistema

- El sistema generará enemigos al inicio de cada oleada.
- La cantidad y dificultad aumentarán progresivamente.
- Existirá un breve descanso entre oleadas.

---

## RF-05 – HUD

**Dependencias:** RG-04

### Requerimiento de Usuario

Como jugador, quiero visualizar mi estado durante la partida para tomar mejores decisiones.

### Requerimientos del Sistema

- El sistema mostrará la vida actual.
- El sistema mostrará la estamina.
- El sistema mostrará el arma equipada.
- El sistema mostrará la oleada actual.
- Toda la información se actualizará en tiempo real.

---

## RF-06 – Menú Principal

**Dependencias:** RG-04

### Requerimiento de Usuario

Como jugador, quiero acceder fácilmente al menú principal para iniciar una partida o modificar opciones.

### Requerimientos del Sistema

- El sistema mostrará las opciones Nueva Partida, Opciones y Salir.
- Permitirá navegar utilizando teclado y mouse.

---

## RF-07 – Pantalla de Resultados

**Dependencias:** RG-04

### Requerimiento de Usuario

Como jugador, quiero conocer mi desempeño al finalizar una partida.

### Requerimientos del Sistema

- Mostrar resultado de la partida.
- Mostrar tiempo sobrevivido.
- Mostrar enemigos eliminados.
- Mostrar oleada alcanzada.
- Permitir jugar nuevamente o regresar al menú principal.

---

## RF-08 – Sistema de Estamina

**Dependencias:** RG-01

### Requerimiento de Usuario

Como jugador, quiero administrar mi estamina para decidir cuándo atacar o esquivar.

### Requerimientos del Sistema

- Atacar consumirá estamina.
- Esquivar consumirá estamina.
- La estamina se recuperará automáticamente con el tiempo.
- Si la estamina llega a cero, el jugador sufrirá una penalización temporal de velocidad.

---

# 6.4 Requerimientos No Funcionales

## RNF-01 – Rendimiento

El videojuego deberá mantener un promedio mínimo de **60 FPS** con hasta **50 enemigos simultáneos** en pantalla.

---

## RNF-02 – Usabilidad

Al menos el **90%** de los jugadores deberá identificar correctamente la barra de vida, estamina y número de oleada en menos de **60 segundos**, sin recibir instrucciones externas.

---

## RNF-03 – Tiempo de respuesta

El tiempo entre la entrada del jugador y la respuesta del sistema no deberá superar los **100 milisegundos** para acciones como movimiento, ataque, cambio de arma y esquiva.

---

# 6.5 Restricciones Técnicas

El desarrollo del videojuego deberá cumplir las siguientes restricciones:

- Unity 2022.3 LTS como motor principal.
- Lenguaje de programación C#.
- Control de versiones mediante GitHub.
- Utilización del nuevo Input System de Unity.
- Uso exclusivo de assets gratuitos o desarrollados por el equipo.

---

# 6.6 Requisitos de Integración

El sistema deberá integrarse con los siguientes componentes de Unity:

- Unity Input System para el manejo de controles.
- Unity Animator para controlar las animaciones del jugador y enemigos.
- Unity UI (UGUI) para implementar el HUD, menús y pantallas.
- Sistema de Audio de Unity para efectos de sonido y música.

---

## Relación con el Product Backlog

Los requerimientos definidos en este documento mantienen trazabilidad directa con las Historias de Usuario del Product Backlog del proyecto.

Cada funcionalidad desarrollada deberá corresponder a uno o más requerimientos funcionales definidos previamente, permitiendo validar que el desarrollo del videojuego cumple con los objetivos establecidos en la ERS.
