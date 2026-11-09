# Especificación de sistemas jugables

Cada sistema debe documentar propósito, reglas, datos, interfaz, dependencias, casos límite y pruebas.

## Exploración e interacción
- Movimiento y colisiones: POR CONFIRMAR.
- Interacción con objetos y personajes: POR CONFIRMAR.
- Diálogos, elecciones y consecuencias: POR CONFIRMAR.
- Puzzles: se han considerado mecánicas tipo puzzle/point-and-click; alcance pendiente.
- Secretos, recompensas y progresión: POR CONFIRMAR.

## Combate

### Dirección confirmada por el creador

El combate debe ser **simple y clásico, tomando como referencia Final Fantasy I**. El creador no busca inventar un sistema de combate nuevo ni introducir mecánicas experimentales.

La personalidad propia de Venequia estará principalmente en el contenido del combate:
- Skills y técnicas.
- Items y objetos utilizables.
- Habilidades de los personajes.
- Enemigos y encuentros con identidad propia.

### Party principal del capítulo I — confirmada

Los cuatro personajes principales de la party del capítulo I son:
- Jotape
- CareLeón
- Yt0
- DD01

### Identidad y habilidades de los personajes — decisiones confirmadas

Cada personaje tendrá **habilidades personalizadas y diferenciadas**. Los repertorios no serán idénticos: cada integrante tendrá técnicas que reflejen su propia identidad y le den una utilidad reconocible dentro del grupo.

- Puede haber habilidades similares entre personajes, pero no tienen que ser copias exactas.
- Las habilidades similares podrán diferenciarse por sus efectos, potencia, coste, alcance, condiciones o utilidad táctica.
- La meta es que cada personaje se sienta distinto y que elegir la composición del equipo tenga interés, sin añadir complejidad innecesaria al sistema clásico.

#### Alcance específico del capítulo I

El creador ha definido una progresión inicial deliberadamente limitada:

- Cada uno de los cuatro personajes principales —Jotape, CareLeón, Yt0 y DD01— aprenderá o tendrá **una sola habilidad especial** durante el capítulo I.
- **Dos personajes** aprenderán su habilidad al alcanzar un nivel determinado.
- **Un personaje** aprenderá su habilidad mediante un objeto.
- **DD01** ya tendrá su habilidad especial cuando se una a la party.
- **Yt0** aprenderá su habilidad especial mediante un objeto.
- Por tanto, **Jotape y CareLeón** aprenderán sus habilidades al subir de nivel; los niveles exactos quedan POR DEFINIR.
- La identidad de cada habilidad, los niveles exactos y el objeto concreto quedan POR DEFINIR.
- Esta limitación corresponde al capítulo I; no determina todavía cuántas habilidades podrán aprender en capítulos posteriores.

La intención es introducir variedad y progresión sin abrumar al jugador ni complicar el balance temprano.

#### Habilidad especial de Yt0 — concepto confirmado

Yt0 es un personaje que cree firmemente en el ejercicio físico y tiene como meta alcanzar una gran fortaleza corporal. Su habilidad especial debe expresar esa identidad y tendrá dos aplicaciones:

- **Exploración:** Yt0 podrá mover rocas u otros objetos pesados que bloqueen caminos, abriendo el acceso a zonas que antes no estaban disponibles. La referencia funcional es la habilidad Strength de Pokémon: mover obstáculos del escenario para desbloquear rutas.
- **Combate:** Yt0 ejecutará un golpe de fuerza extrema que atacará a **todos los enemigos** del grupo contrario.
- **Desbloqueo:** la habilidad se aprenderá mediante un objeto especial, coherente con la progresión ya definida para Yt0.
- **Naturaleza del objeto:** será una bebida que el jugador deberá elaborar combinando **2 o 3 ingredientes**. Los ingredientes concretos, la receta, el nombre de la bebida y cómo se obtienen todavía están POR DEFINIR.

El objetivo de diseño es que una misma habilidad tenga utilidad tanto en el mapa como en batalla, conectando exploración y combate. Para el **capítulo I**, esta es la capacidad inicial prevista: mover los obstáculos pesados definidos para esta etapa y ejecutar un ataque de fuerza contra todos los enemigos. El creador considera que la habilidad podría aumentar de nivel o fortalecerse más adelante, pero esa progresión todavía no está decidida y no debe asumirse como sistema confirmado. El nombre definitivo de la habilidad, el objeto que la enseña, sus parámetros de daño y coste, y las reglas concretas de los obstáculos quedan POR DEFINIR. La referencia a Pokémon es funcional; Venequia tendrá implementación, presentación y nombres propios.

### Principios de implementación

- Mantener una estructura clásica de combate RPG por turnos.
- Priorizar claridad, facilidad de comprensión y ritmo.
- Evitar complejidad innecesaria, sistemas de combos o subsistemas nuevos salvo que el creador los solicite.
- Preferir aprovechar el sistema de batalla existente de RPG Maker MZ si satisface el diseño, antes que desarrollar un motor de combate personalizado.
- Tomar Final Fantasy I como referencia de diseño general; no copiar sus recursos, nombres, textos ni contenido protegido.

### Pendiente de especificación y auditoría

- Presentación exacta de la pantalla de batalla y disposición del grupo: POR CONFIRMAR.
- Orden de turnos y fórmula de velocidad: POR CONFIRMAR.
- Comandos disponibles en batalla: POR CONFIRMAR.
- Tamaño del grupo y número de enemigos: POR CONFIRMAR.
- Recursos (vida, energía, etc.): POR CONFIRMAR.
- Nombre, efecto y función de las habilidades de Jotape, CareLeón y DD01: POR DEFINIR.
- Nombre definitivo, coste y daño de la habilidad de Yt0: POR DEFINIR.
- Objeto que enseña la habilidad de Yt0: POR DEFINIR.
- Bebida que enseña la habilidad de Yt0: se elaborará con 2 o 3 ingredientes; nombre, receta y obtención de ingredientes: POR DEFINIR.
- Tipos de rocas/obstáculos que Yt0 podrá mover en el capítulo I y reglas para desbloquear rutas: POR DEFINIR.
- Si la habilidad de Yt0 tendrá niveles o mejoras en capítulos posteriores: IDEA POSIBLE, NO CONFIRMADA.
- A qué nivel aprenden Jotape y CareLeón sus habilidades: POR DEFINIR.
- Qué objeto permite a Yt0 aprender su habilidad: POR DEFINIR.
- Qué habilidades similares pueden compartir personajes y cómo se diferencian: POR DEFINIR.
- Inventario de items utilizables en batalla: POR CONFIRMAR.
- Enemigos, jefes, estadísticas y patrones: POR CONFIRMAR.
- Condiciones de victoria/derrota: POR CONFIRMAR.
- Recompensas, experiencia y drops: POR CONFIRMAR.
- Encuentros aleatorios o visibles: POR CONFIRMAR.
- Curva de dificultad y balance: POR CONFIRMAR.

### Trabajo del capítulo 1

El creador indica que todavía hay que añadir batallas. Durante la auditoría se elaborará una lista de encuentros necesarios y se vinculará cada uno con su mapa, evento, enemigo, recompensa y propósito dentro del capítulo.

## NPCs y diálogos
- El creador identifica la personalización de NPCs como trabajo pendiente del capítulo 1.
- Apariencia, nombre, ubicación, función, rutina y eventos asociados: documentar NPC por NPC.
- Diálogos: completar y revisar conversaciones según lugar, momento del capítulo y estado de las misiones.
- Decisiones y consecuencias: POR CONFIRMAR.
- Evitar diálogos genéricos; mantener voz, humor y referencias coherentes con el mundo.

## Items e inventario
- El creador identifica completar los items como trabajo pendiente del capítulo 1.
- Los items forman parte de la identidad de Venequia junto con las skills y habilidades de los personajes.
- Inventario de objetos: POR CONFIRMAR.
- Función, descripción, precio, disponibilidad y balance de cada objeto: POR CONFIRMAR.
- Consumibles, equipo, objetos de misión y objetos clave: clasificar durante la auditoría.
- Economía y tiendas: POR CONFIRMAR.

## Progresión
- Niveles y experiencia: POR CONFIRMAR.
- Equipo y consumibles: POR CONFIRMAR.
- Economía y tiendas: POR CONFIRMAR.
- Reclutamiento y disponibilidad de compañeros: POR CONFIRMAR.

## Interfaz y accesibilidad
- Resolución y relación de aspecto: POR CONFIRMAR.
- Idiomas: POR CONFIRMAR.
- Controles y reasignación: POR CONFIRMAR.
- Velocidad de texto, legibilidad y opciones: POR CONFIRMAR.

## Plantilla de sistema
### Nombre
### Objetivo de diseño
### Experiencia esperada del jugador
### Reglas
### Datos y variables
### Eventos / plugins implicados
### Interfaz
### Casos límite
### Riesgos y dependencias
### Pruebas de aceptación
