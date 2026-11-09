# Arquitectura técnica

## Base conocida
- Motor: RPG Maker MZ.
- Lenguaje habitual de plugins de MZ: JavaScript; confirmar versión exacta del motor y runtime del proyecto.
- Plugin externo mencionado: Get Hendrix Realtime Parallax Map Builder. Verificar versión instalada, licencia, ubicación y compatibilidad.

## Inventario pendiente
| Elemento | Versión | Origen/licencia | Uso | Estado |
|---|---|---|---|---|
| RPG Maker MZ | POR CONFIRMAR | Licencia del equipo | Motor | Pendiente |
| Get Hendrix Realtime Parallax Map Builder | POR CONFIRMAR | Compra en itch.io reportada | Parallax / edición de mapas | Pendiente |
| Plugins adicionales | POR CONFIRMAR | POR CONFIRMAR | POR CONFIRMAR | Pendiente |

## Estructura habitual de MZ
La estructura exacta se verificará contra una copia del proyecto real. Puede incluir:
- `Game.rmmzproject`
- `data/`
- `img/`
- `audio/`
- `js/`
- `movies/`
- `fonts/`
- `plugins/` y configuración de plugins dentro de `js/`

No crear estas carpetas en el repositorio como si ya contuvieran el proyecto. La carpeta `GAME/` contiene por ahora instrucciones de incorporación.

## Compatibilidad y dependencias
Registrar:
- Versión de RPG Maker MZ.
- Versión de Node/Electron si aplica a herramientas.
- Plugins y orden de carga.
- Dependencias entre plugins.
- Modificaciones al core.
- Fuentes y licencias de assets.
- Procedimiento de exportación.

## Reglas para cambios técnicos
1. No editar el core de MZ sin una justificación documentada.
2. Preferir plugins propios aislados.
3. Documentar parámetros, comandos, notetags y dependencias.
4. Probar en una copia de desarrollo.
5. Registrar cómo reproducir y revertir cada cambio.
