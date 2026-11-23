# El Puente: registro de partidas

Aquí se guardan las partidas y los puntos de cada jugador de **El Puente**, el juego de Android en el que el Marinero pelea contra Brutorro en un puente para rescatar a la Dama.

Este repositorio **no tiene el código del juego**, solo el registro. Lo escribe la propia app al terminar cada partida y cuando se sale de ella a mitad de una.

- **[CLASIFICACION.md](CLASIFICACION.md)**: ranking de todos los jugadores por su mejor puntuación.
- **`jugadores/<nombre>.md`**: resumen de cada jugador (partidas jugadas, terminadas, victorias, mejor puntuación, nivel en el que retomar) y la lista de sus últimas partidas.
- **`jugadores/<nombre>.json`**: los mismos datos en formato JSON, que es lo que lee la app para recuperar el progreso si cambias de móvil.

## Puntuación

| Acción | Puntos |
|---|---|
| Cada golpe que das en un asalto (o con espinacas) | +10 |
| Cada golpe que te da Brutorro en un asalto | −10 |
| Ganar un asalto | +100 |
| Perder un asalto | −100 |
| Tirar a Brutorro al agua | +1000 |
| Caerte al agua | −1000 |
| Comer espinacas (las del centro o las que te lanza la Dama) | +200 |
| Convertirte en Marinero Coloso (3 latas) | +1500 |
| Súper golpe con las espinacas de la Dama | +500 |
| Puñetazo remolino que alcanza | +300 |
| Combo de patada y gancho | +500 |
| Esquivar un hechizo | +200 |
| Quedarte hechizado | −300 |
| Coger una espinaca roja de la Bruja Blanca | +300 |
| Ganar una vida tirando a Brutorro por tu lado | +1000 |
| Un rayo te carga y das el golpe eléctrico | +300 |
| Un rayo carga a Brutorro y te da el golpe eléctrico | −300 |
| El Bebé le tira un ladrillo a Brutorro | +100 |
| Brutorro te pilla al huir | −50 |
| Brutorro tira tus espinacas al mar | −100 |
| Pasar de nivel | +2000 |
| Ganar el nivel 10 | +10000 |

La puntuación de una partida nunca baja de 0.

## Estados de una partida

- **Victoria**: ganaste los 10 niveles.
- **Game over**: perdiste las 3 vidas. Se puede **retomar en el nivel** en el que te quedaste.
- **En curso**: saliste de la app a mitad de partida.
- **Sin terminar**: empezaste otra partida sin acabar la anterior. También se puede retomar.

Las partidas de prueba (código secreto) no se registran.
