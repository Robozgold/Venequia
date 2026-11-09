# Flujo de trabajo — GitHub, Codex y RPG Maker MZ

## Objetivo
Tener historial, copias revisables y documentación compartida sin arriesgar el proyecto original.

## Reglas de seguridad
- Mantener una copia de respaldo fuera del repositorio.
- No hacer el primer commit con la única copia de trabajo.
- Nunca subir contraseñas, tokens, claves, datos personales o archivos de cuenta.
- No incorporar archivos de plugins comprados si sus condiciones no permiten redistribución.
- Revisar tamaño y cantidad de archivos antes de subir assets.
- No forzar pushes ni borrar historial.
- No aceptar cambios automáticos sin revisar el diff y probar el juego.

## Organización Git propuesta
- `main`: versión estable y revisada.
- `develop`: integración de trabajo (crear cuando el flujo esté listo).
- `feature/nombre-corto`: trabajo aislado.
- `fix/nombre-corto`: correcciones.
- `docs/nombre-corto`: documentación.

Para un equipo pequeño puede bastar inicialmente con ramas de trabajo y Pull Requests hacia `main`.

## Flujo de cambio
1. Identificar objetivo, alcance y archivos afectados.
2. Crear una rama desde el estado estable.
3. Hacer un cambio pequeño.
4. Revisar diff y archivos nuevos.
5. Ejecutar pruebas relevantes en una copia del proyecto.
6. Documentar resultado y limitaciones.
7. Abrir Pull Request.
8. Revisar y aprobar antes de integrar.

## Codex
Codex debe recibir instrucciones específicas:
- leer `AGENTS.md` y la documentación pertinente;
- inspeccionar antes de modificar;
- no borrar ni reformatear masivamente;
- mostrar plan y archivos afectados;
- mantener cambios acotados;
- añadir pruebas o pasos manuales de validación;
- no modificar `main` directamente.

## Qué no subir de entrada
Revisar antes de incluir:
- cachés, logs, temporales y archivos generados;
- partidas guardadas y datos locales;
- ejecutables/exportaciones completas;
- dependencias generadas que puedan reconstruirse;
- archivos pesados que requieran Git LFS;
- plugins o assets con restricciones de licencia.

El `.gitignore` se ajustará después de inspeccionar una copia real del proyecto. No ignorar indiscriminadamente datos de MZ que puedan ser necesarios.
