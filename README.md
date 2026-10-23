# Horario de Mi Rutina

La app **Mi Rutina** lee `horario.json` cada vez que se abre con internet.
Si cambias algo aquí, el teléfono lo recibe solo y reprograma los avisos.
Tus avances (lo que marcas, repeticiones, racha) se guardan en el teléfono, no aquí.

- `days` tiene 7 listas, empezando por **domingo** (0) hasta **sábado** (6).
- Cada actividad tiene `id`, `t` (hora "HH:MM"), `end` opcional, `cat`, `title`, `sub`
  y `steps` (lista de pasos) o `items` (pasos marcables).
- No cambies el `id` de una actividad que ya existe: así se conserva lo que marcaste.
- Si el archivo queda mal escrito, la app lo ignora y sigue con el último horario bueno.
