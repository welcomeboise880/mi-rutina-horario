# Horario de Mi Rutina

La app **Mi Rutina** lee `horario.json` cada vez que se abre con internet.
Si cambias algo aquí, el teléfono lo recibe solo y reprograma los avisos.
Tus avances (lo que marcas, repeticiones, racha) se guardan en el teléfono, no aquí.

- `days` tiene 7 listas, empezando por **domingo** (0) hasta **sábado** (6).
- Cada actividad tiene `id`, `t` (hora "HH:MM"), `end` opcional, `cat`, `title`, `sub`
  y `steps` (lista de pasos) o `items` (pasos marcables).
- No cambies el `id` de una actividad que ya existe: así se conserva lo que marcaste.
- Si el archivo queda mal escrito, la app lo ignora y sigue con el último horario bueno.

## Días especiales (una sola vez)

`fechas` cambia solo un día del calendario. Al día siguiente regresa el horario normal.

```json
"fechas": {
  "2026-10-29": { "nota": "Voy al cine", "blocks": [ ...actividades de ese día... ] }
}
```

## Entrenamiento y comida

- `entreno` tiene la rutina de la pestaña **Entreno**: `dias` (7 sesiones, empezando por domingo),
  `sesiones` (ejercicios con series, reps y descanso en segundos) y `ejercicios` (cómo se hace cada uno).
- `menu` tiene la pestaña **Comida**: `dias` (desayuno, colación, comida y cena de domingo a sábado),
  la lista del súper y las reglas del plato.
- No cambies el `id` de un ejercicio que ya existe: así se conservan tus kilos y repeticiones anteriores.
- Si alguna de estas dos partes queda mal escrita, la app usa la que trae de fábrica.
