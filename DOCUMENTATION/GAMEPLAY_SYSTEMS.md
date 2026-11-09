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


#### Consumo de casetes — decisión confirmada

Los casetes son **objetos consumibles de un solo uso**. Cuando DD01 reproduce un casete, este se gasta y se elimina del inventario; no puede volver a utilizarse. Esta regla se aplica a los casetes del capítulo I y debe reflejarse en la descripción del objeto y en la lógica de inventario/combate.


#### Límite de uso en combate — decisión confirmada

En cada batalla solo se podrá utilizar **un casete**. Una vez reproducido, no se podrá activar otro casete durante ese mismo combate. El efecto del casete elegido permanece durante toda la batalla. Esta regla evita combinar mejoras y mantiene el sistema sencillo.


#### Obtención de uno de los casetes — Patinetada y banda PUNK T.A.M.P. — confirmación del creador

En Valle Pao se celebra una **Patinetada** para conmemorar los «sopotocientos años» del lugar. Una de las atracciones del evento es la presentación en vivo de la banda **PUNK T.A.M.P.**, cuyo nombre significa **«Tírame algo menos piedra»**.

Durante la celebración hay una tienda que vende mercancía de la banda. En esa tienda el jugador podrá conseguir uno de los casetes asociados al sistema musical de DD01. El creador aún no ha concretado si el casete se regala, se obtiene como parte de una compra u otra interacción con la tienda; el método exacto queda POR DEFINIR.


#### Obtención de otro casete — Rashid, compañero del DJ — confirmación del creador

El DJ del Valle Pao tiene un compañero llamado **Rashid**. Rashid podrá obsequiar al jugador uno de los casetes musicales. La forma concreta de activar/recibir el regalo (diálogo, misión, condición o momento) queda POR DEFINIR.


#### Obtención del tercer casete — casa de Valle Pao — confirmación del creador

El tercer casete podrá encontrarse dentro de una de las casas de Valle Pao. Como posible presentación dentro del escenario, estará guardado dentro de un **radio portátil/reproductor portátil de casetes**. La casa concreta y la interacción para recogerlo quedan POR DEFINIR.


#### Interacción para conseguir el tercer casete — confirmación del creador

El jugador encontrará el radio portátil dentro de una casa de Valle Pao. Al interactuar con el radio, obtendrá directamente el casete que está dentro. No se ha definido todavía cuál casa concreta lo contiene.


#### Curación de DD01 — progresión confirmada

- La curación inicial de DD01 será **individual**: podrá curar a un personaje de la party cada vez.
- A medida que DD01 suba de nivel, se desbloqueará la opción de que aprenda una habilidad de **curación para todo el grupo**.
- El nivel exacto en que se ofrecerá/aprenderá la curación grupal, su coste, potencia y condiciones quedan POR DEFINIR.
- Esta progresión amplía el rol de apoyo de DD01 de forma gradual. Debe coordinarse con la regla general de una habilidad especial por personaje durante el capítulo I; el alcance temporal y el momento de aprendizaje de la curación grupal aún necesitan concretarse.


#### Posibles capacidades de exploración y conocimiento de DD01 — ideas por explorar

El creador plantea que, por ser una inteligencia artificial/robot con capacidades de conocimiento superiores, DD01 podría aportar utilidades de exploración y comprensión que los demás integrantes no tienen. Entre las posibilidades mencionadas:
- Detectar objetos ocultos o elementos de interés en el entorno.
- Interpretar, traducir o leer idiomas, escrituras, códigos o textos que otros miembros de la party no entienden.

Estas capacidades son **ideas propuestas para explorar**, no habilidades aprobadas ni sistemas cerrados. Falta decidir cuáles tendrá DD01 realmente, cómo se activan, qué límites tienen y si se desbloquean por historia, nivel u objetos. Su función debe enriquecer la exploración y resolver situaciones concretas sin quitar protagonismo a los demás personajes.


#### Exclusividad de las capacidades de exploración de DD01 — dirección confirmada

El creador confirma que quiere que ciertas capacidades de exploración y conocimiento sean **exclusivas de DD01**. Esto permitirá crear lugares, secretos, textos, mecanismos o dispositivos que solo puedan descubrirse, interpretarse o utilizarse cuando DD01 esté en la party. La idea de que DD01 deba estar presente para acceder a estos contenidos queda confirmada como dirección de diseño; cuáles capacidades concretas se implementarán y sus límites siguen POR DEFINIR.


#### Conexión de DD01 con computadoras y máquinas — alcance aplazado

La posibilidad de que DD01 se conecte directamente con computadoras, terminales u otras máquinas se considera una capacidad futura, pero el creador señala que **quizá no sea necesaria en el capítulo I** para mantener el alcance sencillo. Por ahora queda fuera de los requisitos del primer capítulo y se conserva como posibilidad para capítulos posteriores, sujeta a necesidades narrativas y de diseño.

Para el capítulo I, las capacidades de exploración que se priorizarán para evaluar son la detección de objetos ocultos y la lectura/interpretación de textos que otros personajes no comprenden. Su implementación concreta aún debe definirse.


#### Personalidad y voz de DD01 — confirmación del creador

DD01 tendrá una personalidad reconocible al comunicarse. Su condición de inteligencia artificial/robot se reflejará en comentarios **curiosos e inteligentes**, además de **humor involuntario**. No será un robot inexpresivo ni un simple dispositivo funcional: sus observaciones, interpretaciones literales y comentarios podrán aportar humor y carácter a los diálogos del grupo. Los rasgos concretos de su voz, expresiones recurrentes y evolución durante la historia quedan POR DEFINIR.


#### Curiosidad de DD01 por la humanidad — confirmación del creador

DD01 **sabe que es un robot** y no está confundido respecto a su naturaleza. Sin embargo, siente interés por conocer las relaciones humanas y comprender qué significa ser humano. El creador cita Astro Boy como referencia de tono/concepto para esta dimensión del personaje. La referencia orienta la curiosidad, sensibilidad y relación del robot con la humanidad; DD01 debe conservar identidad, historia, voz y desarrollo propios de Venequia, sin copiar el personaje ni sus elementos protegidos.

Esta curiosidad puede expresarse mediante preguntas, observaciones y conversaciones sobre amistad, afecto, nostalgia, enfado, sacrificio y otras experiencias humanas. Su comprensión y evolución emocional a lo largo de la historia quedan POR DEFINIR.


#### Evolución gradual de DD01 — dirección narrativa aceptada

El creador considera buena la idea de que, a lo largo de los capítulos, DD01 vaya comprendiendo mejor las emociones y relaciones humanas y desarrolle una sensibilidad propia. Se registra como **dirección narrativa aceptada** para su arco a largo plazo, no como una transformación ya detallada. Los momentos, límites y cambios concretos de esta evolución se definirán al desarrollar la historia de cada capítulo.


### Exploración y reclutamiento de Yt0: prueba de Fuerza de Loco

La incorporación de Yt0 se vincula a un desafío de exploración en el gimnasio de Valle Pao:

- Yt0 está concentrado en su rutina de ejercicios y no la interrumpe por nada del mundo.
- Los NPC transmiten su disciplina y seriedad con el entrenamiento, y algunos introducen la habilidad **Fuerza de Loco**, que permite mover objetos muy pesados.
- En el gimnasio hay una roca o balón medicinal que nadie puede mover.
- Un NPC da una pista para obtener la habilidad mediante una bebida especial cuyos ingredientes debe reunir el jugador.
- Tras preparar y beber la mezcla, JP obtiene Fuerza de Loco y puede mover el objeto pesado del gimnasio.
- Al presenciarlo, Yt0 interrumpe su entrenamiento, pregunta cómo lo consiguió JP y, motivado por aprender la habilidad, se une a la party.

La habilidad ya está definida conceptualmente para tener dos usos: desplazar obstáculos pesados en el mapa y ejecutar un ataque que afecta a todos los enemigos en combate. La secuencia del gimnasio presenta y demuestra primero su utilidad de exploración.

**Pendiente de diseño:** ingredientes, receta, NPC que da la pista, objeto exacto que se mueve y evento de preparación/consumo. El momento de aprendizaje de Yt0 ya está decidido: aprende Fuerza de Loco al subir de nivel; queda por definir el nivel concreto. Mantener la implementación sencilla y aprovechar eventos y capacidades nativas de RPG Maker MZ siempre que sea posible.


#### Regla definitiva de aprendizaje: JP solo obtiene Fuerza de Loco temporalmente

La bebida de la prueba del gimnasio concede a **JP** Fuerza de Loco de manera **temporal y excepcional**. Uno de los ingredientes de la mezcla no es exactamente el ingrediente habitual requerido para esa bebida, pero puede funcionar como sustituto y producir el efecto. JP utiliza la fuerza obtenida para mover la roca o el balón medicinal del gimnasio; inmediatamente después de superar esa prueba, pierde la habilidad y no vuelve a tenerla durante el juego.

**Yt0 es el único personaje que aprende y conserva Fuerza de Loco como habilidad propia.** Se une a la party sin esta habilidad y la aprende al subir de nivel, reflejando su disciplina y progreso mediante el entrenamiento. El nivel exacto de aprendizaje queda POR DEFINIR. Esta progresión puede implementarse mediante el aprendizaje de habilidades por nivel del sistema nativo de RPG Maker MZ.

Por tanto, la bebida de JP sirve para resolver el desafío de reclutamiento, no para otorgarle una habilidad permanente ni para definir por sí sola el aprendizaje de Yt0.


#### Obstáculo de Fuerza de Loco en las Cuevas del Indio

Además de la roca o balón medicinal del gimnasio, habrá una segunda roca pesada dentro de las **Cuevas del Indio** que bloqueará un camino. Para moverla se requiere que **Yt0 forme parte de la party y haya aprendido Fuerza de Loco** al subir de nivel.

La comprobación jugable debe considerar ambas condiciones: presencia de Yt0 en el grupo y aprendizaje de la habilidad. Así, la habilidad funciona como requisito de exploración y recompensa por progresión de nivel. Quedan por definir la ubicación exacta del obstáculo, el contenido o ruta que desbloquea y si es obligatorio u opcional.


### Distribución de encuentros del capítulo I

Las **Cuevas del Indio** serán la zona principal de combate del capítulo I. La mayoría de los encuentros tendrán lugar dentro de esta mazmorra y enfrentarán al grupo con animales, criaturas o especies extrañas que habitan allí.

Antes de entrar puede haber aproximadamente **dos encuentros con animales salvajes** en los alrededores, para introducir al jugador al combate. Estos encuentros serán minoritarios frente a los que se desarrollarán dentro de las cuevas.

**Pendiente de diseño y balance:** lista de enemigos, estadísticas, habilidades, recompensas, distribución por zonas, frecuencia de encuentros y curva de dificultad. La concentración de combates en una mazmorra permite introducir progresivamente los sistemas y controlar el ritmo del capítulo.


### Encuentros visibles con activación por proximidad

El creador confirma que los enemigos de las Cuevas del Indio serán **visibles directamente en el mapa**, siguiendo como referencia el sistema de encuentros de Pokémon:

- Las criaturas y enemigos aparecen como eventos o sprites visibles durante la exploración.
- Cuando el jugador se acerca lo suficiente a un enemigo, el encuentro se activa automáticamente y comienza la batalla.
- No hace falta interactuar ni pulsar un botón para iniciar el combate.
- No se utilizarán encuentros aleatorios al caminar como sistema principal de la mazmorra.

La distancia o condición exacta que activa el encuentro, el comportamiento de persecución de los enemigos y si el jugador puede evitar algunos encuentros mediante rutas alternativas quedan POR DEFINIR. La referencia a Pokémon es funcional; la presentación y comportamiento concretos serán propios de Venequia.


#### Comportamientos de enemigos visibles

El creador confirma que los enemigos visibles de las Cuevas del Indio podrán tener distintos comportamientos:

- **Enemigos móviles/perseguidores:** algunas criaturas detectarán a JP y se acercarán a él para iniciar el combate al alcanzarlo o entrar en su rango de contacto.
- **Enemigos bloqueadores:** otras criaturas permanecerán en puntos estratégicos, como pasillos o caminos estrechos, impidiendo el avance. El jugador deberá derrotarlas para despejar el paso. Una vez derrotadas, desaparecerán del mapa y dejarán libre esa ruta.

Esta variedad permite que algunos encuentros dependan del movimiento y detección del jugador, mientras que otros funcionen como bloqueos de progresión dentro de la mazmorra. Los rangos de detección, velocidades, condiciones de activación y persistencia del enemigo derrotado quedan POR DEFINIR.
