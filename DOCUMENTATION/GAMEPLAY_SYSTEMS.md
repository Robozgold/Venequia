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

#### DD01 — identidad y sistema musical — concepto confirmado

DD01 es un robot creado por el **Prof. Bichito** como robot de exploración. No fue diseñado originalmente para combatir. Su identidad inicial en la party está orientada al apoyo y la **curación**; a medida que avance el juego, irá aprendiendo habilidades de batalla.

El creador también propone un sistema de **casetes musicales**:
- El jugador podrá encontrar casetes durante la aventura.
- **Únicamente DD01** podrá reproducirlos.
- Al reproducir un casete durante una batalla, cambiará la música de combate.
- La música otorgará mejoras de atributos al grupo, por ejemplo, ataque o defensa.

La idea une la identidad de DD01 como robot con una mecánica de apoyo grupal basada en música. El creador deja la duración a criterio de la implementación más sencilla. Como opción inicial de diseño, se propone que el efecto dure **toda la batalla** y termine al finalizar el combate, evitando tener que contar turnos. Esta duración queda como preferencia práctica, sujeta a comprobar la implementación en RPG Maker MZ. También quedan POR DEFINIR si los casetes son consumibles o reutilizables, qué atributos puede mejorar cada uno, si los efectos se acumulan o se sustituyen, cómo se seleccionan y activan en batalla, y cómo se obtienen los casetes. La progresión y cantidad de habilidades de combate que DD01 aprenderá en cada capítulo también quedan por concretar.

#### Habilidad especial de Yt0 — concepto confirmado

Yt0 es un personaje que cree firmemente en el ejercicio físico y tiene como meta alcanzar una gran fortaleza corporal. Su habilidad especial debe expresar esa identidad y tendrá dos aplicaciones:

- **Exploración:** Yt0 podrá mover rocas u otros objetos pesados que bloqueen caminos, abriendo el acceso a zonas que antes no estaban disponibles. La referencia funcional es la habilidad Strength de Pokémon: mover obstáculos del escenario para desbloquear rutas.
- **Combate:** Yt0 ejecutará un golpe de fuerza extrema que atacará a **todos los enemigos** del grupo contrario.
- **Desbloqueo:** la habilidad se aprenderá mediante un objeto especial, coherente con la progresión ya definida para Yt0.
- **Naturaleza del objeto:** será una bebida que el jugador deberá elaborar combinando **2 o 3 ingredientes**. La combinación incluirá **un ingrediente especial y uno cotidiano**. El ingrediente especial podrá conseguirse durante la exploración o recibirlo de un NPC a cambio de entregarle otro objeto; queda por definir cuál de esas vías se usará (o si se usarán ambas). Si se usan 2 o 3 ingredientes en total, y cuáles serán, queda POR DEFINIR. El ingrediente cotidiano podrá obtenerse por cualquiera de estas vías: comprarlo en una tienda, recogerlo del escenario o conseguirlo de un NPC. Para evitar añadir complejidad, la preferencia actual del creador es que no haga falta acudir a un lugar especial: el jugador entregaría los ingredientes a Yt0 y él mismo prepararía la bebida. Esta solución queda como dirección preferida, pendiente de concretar su interacción en el juego. La receta, el nombre de la bebida y los ingredientes concretos todavía están POR DEFINIR.

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
- Nombre y efecto de las habilidades de Jotape y CareLeón: POR DEFINIR.
- Habilidad inicial de apoyo/curación de DD01 y su progresión de habilidades de combate: concepto definido, detalles POR DEFINIR.
- Sistema de casetes musicales de DD01: casetes encontrados durante la aventura; solo DD01 puede reproducirlos; al activarlos cambia la música de batalla y mejora atributos del grupo (por ejemplo, ataque o defensa). Duración: preferencia práctica por mantener el efecto durante toda la batalla y retirarlo al terminar, si resulta sencillo de implementar; sujeto a comprobación técnica. Consumo, selección, efectos concretos y reglas de acumulación: POR DEFINIR.
- Nombre definitivo, coste y daño de la habilidad de Yt0: POR DEFINIR.
- Objeto que enseña la habilidad de Yt0: POR DEFINIR.
- Bebida que enseña la habilidad de Yt0: incluirá un ingrediente especial y uno cotidiano. El especial podrá encontrarse explorando o conseguirse de un NPC a cambio de otro objeto; la vía concreta (o combinación de vías) queda por decidir. El ingrediente cotidiano podrá comprarse en una tienda, recogerse del escenario o conseguirse de un NPC. Número total de ingredientes (2 o 3), identidades, nombre y receta: POR DEFINIR.
- Preparación de la bebida: preferencia actual por una solución sencilla, sin lugar especial de elaboración; el jugador entregaría los ingredientes a Yt0 para que él prepare la bebida. Interacción exacta: POR DEFINIR.
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


#### Grupos musicales del Valle Pao — confirmación del creador

En el Valle Pao, lugar donde comienza el juego, hay dos grupos de NPCs vinculados a la música:
- Un DJ.
- Una banda de punk con estética/sonido de 8 bits.

El creador ya ha compuesto varias pistas musicales con Suno específicamente para estos NPCs. Por tanto, estas canciones pertenecen a artistas/grupos existentes dentro del mundo de Venequia y pueden servir como base para los casetes musicales que DD01 reproduce en combate. La asignación de canciones concretas a casetes, sus efectos de atributos y las reglas de obtención/uso siguen POR DEFINIR.


#### Disponibilidad de los casetes en el capítulo I — decisión confirmada

- Durante el capítulo I, el jugador podrá conseguir aproximadamente **3 casetes**.
- Los casetes podrán encontrarse/obtenerse antes de que DD01 se una a la party, pero **no podrán utilizarse mientras DD01 no forme parte del grupo**.
- Al incorporarse DD01, el jugador podrá utilizar los casetes que haya conseguido, ya que únicamente este personaje puede reproducirlos.
- La cantidad indicada es aproximada (unos tres) para el primer capítulo.
- La ubicación y método de obtención de cada casete, y el efecto musical/atributo de cada pista, siguen POR DEFINIR.
