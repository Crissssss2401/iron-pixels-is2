# Especificación del Caso de Uso – CU-01

| Información | Detalle |
|-------------|---------|
| **Responsable** | Cristian Sahón |
| **Rol** | Scrum Master – Líder del Equipo |
| **Proyecto** | Dead Harvest |
| **Documento** | Especificación del Caso de Uso CU-01 |
| **Versión** | 1.0 |
| **Fecha** | 04/08/2026 |

---

# CU-01 – Atacar cuerpo a cuerpo

## Objetivo

Permitir que el jugador ataque utilizando el arma cuerpo a cuerpo equipada para eliminar enemigos, protegerse de las oleadas y continuar avanzando durante la partida.

---

## Descripción

Este caso de uso describe la interacción entre el jugador y el sistema cuando se ejecuta un ataque cuerpo a cuerpo. El sistema verifica que el jugador cumpla las condiciones necesarias para realizar la acción, ejecuta la animación correspondiente, detecta las colisiones con los enemigos y aplica el daño de acuerdo con las características del arma equipada.

---

## Actor Principal

- Jugador.

---

## Actores Secundarios

- Sistema del Juego.

---

## Precondiciones

- El jugador ha iniciado una partida.
- Existe un arma cuerpo a cuerpo equipada.
- El jugador tiene al menos la cantidad mínima de estamina necesaria para realizar un ataque.
- Existe al menos un enemigo activo dentro de la partida.

---

## Postcondiciones

- La estamina del jugador disminuye según el costo del ataque.
- El enemigo recibe daño si se encuentra dentro del rango del arma.
- Si la vida del enemigo llega a cero, este es eliminado del escenario.
- El sistema actualiza la información mostrada en el HUD.

---

# Flujo Principal

1. El jugador presiona el botón de ataque.
2. El sistema verifica que exista un arma equipada.
3. El sistema verifica la cantidad de estamina disponible.
4. El sistema reproduce la animación correspondiente al arma equipada.
5. Se activa el área de impacto (Hitbox).
6. El sistema detecta los enemigos que se encuentran dentro del alcance del ataque.
7. Se calcula el daño correspondiente según el arma utilizada.
8. El sistema reduce la vida del enemigo impactado.
9. Se reproducen los efectos visuales y de sonido asociados al ataque.
10. Se actualiza la información del HUD.
11. El caso de uso finaliza.

---

# Flujos Alternativos

### FA-01 – No hay enemigos en el rango de ataque

En caso de que no exista ningún enemigo dentro del área de impacto, el sistema ejecuta la animación del ataque, consume la estamina correspondiente y finaliza el caso de uso sin aplicar daño.

---

### FA-02 – El enemigo sobrevive al ataque

Si el enemigo aún conserva puntos de vida después de recibir el daño, permanece activo dentro de la partida y continúa ejecutando su comportamiento definido por la Inteligencia Artificial.

---

# Flujos de Excepción

### FE-01 – Estamina insuficiente

Si el jugador no posee suficiente estamina para ejecutar el ataque, el sistema cancela la acción, muestra la penalización correspondiente y no aplica daño.

---

### FE-02 – El jugador ha sido derrotado

Si el jugador pierde toda su vida antes de ejecutar el ataque, el sistema finaliza la partida y muestra la pantalla de resultados.

---

# Requerimientos Funcionales Relacionados

- RF-01 – Ataque cuerpo a cuerpo.
- RF-08 – Sistema de estamina.

---

# Casos de Uso Relacionados

- CU-02 – Cambio de armamento.
- CU-03 – Inteligencia Artificial de los enemigos.

---

# Reglas de Negocio Relacionadas

- RN-01 – La estamina nunca podrá ser negativa ni superar su valor máximo.
- RN-03 – Cuando la estamina llegue a cero, la velocidad de ataque disminuirá hasta recuperar un valor mínimo.
- RN-04 – Los enemigos únicamente recibirán daño cuando exista una colisión válida entre el arma y su Hitbox.

---

# Observaciones

Este caso de uso representa una de las mecánicas principales del videojuego y constituye el núcleo del sistema de combate. Su implementación deberá mantenerse alineada con el requerimiento funcional RF-01 definido en la ERS y con la historia de usuario HU-02 del Product Backlog.

Además, este caso de uso servirá como base para el desarrollo del sistema de combate, las pruebas funcionales y la implementación de la Inteligencia Artificial de los enemigos durante las siguientes iteraciones del proyecto.
