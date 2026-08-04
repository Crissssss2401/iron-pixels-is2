# Especificación del Caso de Uso

| Información | Detalle |
|-------------|---------|
| **Responsable** | Cristian Sahón |
| **Rol** | Scrum Master – Líder del Equipo |
| **Proyecto** | Dead Harvest |
| **Código** | CU-01 |
| **Nombre** | Atacar cuerpo a cuerpo |
| **Historia de Usuario Relacionada** | HU-02 – Ataque cuerpo a cuerpo |
| **Requerimiento Funcional** | RF-01 – Ataque cuerpo a cuerpo |
| **Versión** | 1.0 |
| **Fecha** | 04/08/2026 |

---

# CU-01 – Atacar cuerpo a cuerpo

## Objetivo

Permitir que el jugador ejecute un ataque utilizando el arma cuerpo a cuerpo equipada para eliminar enemigos y sobrevivir a las diferentes oleadas del juego.

---

## Descripción General

Este caso de uso representa una de las mecánicas principales del videojuego **Dead Harvest**. Durante la partida, el jugador podrá utilizar el arma equipada para atacar a los enemigos que se encuentren dentro del alcance del arma. El sistema verificará que el ataque pueda ejecutarse, calculará las colisiones con los enemigos y aplicará el daño correspondiente, actualizando el estado del combate y la información mostrada en el HUD.

---

## Actor Principal

- Jugador.

---

## Actor Secundario

- Sistema del Juego.

---

# Precondiciones

- El jugador ha iniciado una partida.
- Existe un arma cuerpo a cuerpo equipada.
- El jugador posee suficiente estamina para ejecutar el ataque.
- El personaje se encuentra con vida.
- Existe al menos un enemigo activo dentro del escenario.

---

# Flujo Principal

1. El jugador presiona el botón de ataque.
2. El sistema verifica que exista un arma equipada.
3. El sistema comprueba que el jugador tenga estamina suficiente.
4. Se ejecuta la animación correspondiente al arma equipada.
5. Se activa temporalmente la Hitbox del arma.
6. El sistema detecta si existe colisión con uno o más enemigos.
7. Se calcula el daño correspondiente según el arma utilizada.
8. El sistema reduce la vida del enemigo impactado.
9. Si la vida del enemigo llega a cero, el enemigo es eliminado.
10. Se reproducen los efectos visuales y sonoros correspondientes al ataque.
11. El sistema actualiza el HUD mostrando los cambios de vida, estamina y estado del combate.
12. Finaliza el caso de uso.

---

# Flujos Alternativos

## FA-01 – No existe ningún enemigo dentro del alcance

Si no existe ningún enemigo dentro del área de impacto, el sistema ejecutará la animación del ataque y consumirá la estamina correspondiente, pero no aplicará daño.

---

## FA-02 – El enemigo sobrevive

Si el enemigo conserva puntos de vida después de recibir el daño, continuará ejecutando normalmente su comportamiento definido por la Inteligencia Artificial.

---

# Flujos de Excepción

## FE-01 – Estamina insuficiente

Si el jugador intenta atacar sin disponer de la estamina mínima requerida, el sistema cancelará la acción y no ejecutará el ataque.

---

## FE-02 – Jugador derrotado

Si el jugador pierde toda su vida antes de completar el ataque, el sistema finalizará la partida y mostrará la pantalla de resultados.

---

# Postcondiciones

- La estamina del jugador disminuye.
- La vida del enemigo se actualiza correctamente.
- El enemigo es eliminado si su vida llega a cero.
- El HUD refleja inmediatamente los cambios producidos durante el combate.
- El sistema queda listo para recibir una nueva acción del jugador.

---

# Requerimientos Relacionados

- RF-01 – Ataque cuerpo a cuerpo.
- RF-08 – Sistema de estamina.

---

# Historia de Usuario Relacionada

**HU-02 – Ataque cuerpo a cuerpo**

> Como jugador, quiero atacar cuerpo a cuerpo para eliminar zombis y sobrevivir durante las oleadas.

---

# Reglas de Negocio Relacionadas

- RN-01 – La estamina nunca podrá ser negativa ni superar su valor máximo.
- RN-03 – Si la estamina llega a cero, la velocidad de ataque disminuirá temporalmente.
- RN-04 – El daño solo podrá aplicarse cuando exista una colisión válida entre la Hitbox del arma y el enemigo.

---

# Prioridad

**Must Have**

---

# Observaciones

Este caso de uso corresponde a una de las funcionalidades implementadas durante el **Sprint 1** del proyecto y mantiene trazabilidad directa con el **Issue #2 (HU-02)** del GitHub Project y con el **RF-01** definido en la Especificación de Requisitos de Software.

La implementación de este caso de uso constituye la base del sistema de combate del videojuego y servirá como referencia para las pruebas funcionales y la integración con la Inteligencia Artificial de los enemigos.
