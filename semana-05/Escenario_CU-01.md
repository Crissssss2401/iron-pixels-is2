# CU-01 – Atacar cuerpo a cuerpo

## Código
CU-01

## Nombre
Atacar cuerpo a cuerpo

## Objetivo
Permitir que el jugador ataque a los zombis utilizando un arma
cuerpo a cuerpo para causar daño y eliminarlos durante la partida.

## Descripción
Este caso de uso describe el proceso que ocurre cuando el jugador
realiza un ataque cuerpo a cuerpo contra un enemigo.

## Actor principal
Jugador.

## Actores secundarios
Sistema del juego.

## Precondiciones
- El jugador debe haber iniciado una partida.
- El personaje debe estar con vida.
- Debe tener un arma cuerpo a cuerpo equipada.
- Debe contar con suficiente estamina para atacar.

## Flujo principal
1. El jugador presiona el botón de ataque.
2. El sistema verifica que tenga un arma cuerpo a cuerpo equipada.
3. El sistema comprueba que tenga suficiente estamina.
4. El personaje realiza la animación de ataque.
5. El sistema verifica si el ataque alcanza a un enemigo.
6. Si existe un impacto, se aplica el daño correspondiente.
7. La vida del enemigo disminuye.
8. El sistema verifica la vida restante del enemigo.
9. Si su vida llega a cero, el enemigo es eliminado.
10. Se descuenta la estamina utilizada.
11. El HUD actualiza la información correspondiente.
12. El jugador puede continuar realizando acciones.

## Flujos alternativos

### FA-01 – El ataque no alcanza a un enemigo
1. El jugador realiza el ataque.
2. El sistema no detecta ningún enemigo dentro del alcance.
3. El ataque termina sin causar daño.
4. Se consume la estamina correspondiente.
5. El jugador puede continuar con la partida.

### FA-02 – El enemigo sobrevive al ataque
1. El ataque alcanza al enemigo.
2. El sistema aplica el daño.
3. La vida del enemigo disminuye, pero no llega a cero.
4. El enemigo continúa activo.

## Flujos de excepción

### FE-01 – Estamina insuficiente
1. El jugador intenta atacar.
2. El sistema detecta que no tiene suficiente estamina.
3. El ataque no se realiza.
4. El jugador debe esperar a recuperar estamina.

### FE-02 – Jugador derrotado
1. La vida del jugador llega a cero.
2. El personaje pasa al estado derrotado.
3. El jugador ya no puede realizar ataques.
4. La partida finaliza.

## Postcondiciones
- La estamina utilizada durante el ataque queda descontada.
- Si el ataque alcanzó al enemigo, su vida disminuye.
- Si la vida del enemigo llegó a cero, este es eliminado.
- El HUD refleja los cambios correspondientes.
- El jugador puede continuar jugando mientras permanezca con vida.

## Requerimientos relacionados
- RF-01 – Ataque cuerpo a cuerpo.
- RF-05 – HUD.
- RF-08 – Sistema de estamina.
- HU-03 – Ataque cuerpo a cuerpo.

## Observaciones
El ataque cuerpo a cuerpo es una de las mecánicas principales de
Dead Harvest. Su funcionamiento está relacionado con el sistema de
estamina, por lo que el jugador deberá administrar este recurso durante
el combate.

Este caso de uso también sirve como referencia para los diagramas
de actividades, secuencia, comunicación y estados relacionados con
el comportamiento del jugador.
