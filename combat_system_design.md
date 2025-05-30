# Diseño del Sistema de Combate - Euskal Herria

Este documento detalla las mecánicas de combate para el protagonista, Aitor, y otros elementos fundamentales del sistema.

## I. Combate con Espada (Aitor)

El combate con espada de Aitor se centrará en la agilidad, la precisión y la gestión de recursos (Stamina).

### 1. Ataques Básicos

*   **Combo Ligero (3 Golpes):**
    *   **Activación:** Pulsaciones sucesivas del botón de ataque principal (ej: `Click Izquierdo Ratón` / `Botón X/Cuadrado Mando`).
    *   **Golpe 1:** Un tajo rápido y vertical. Daño bajo, buena velocidad de inicio.
    *   **Golpe 2:** Un tajo horizontal. Daño moderado, cubre un arco ligeramente mayor.
    *   **Golpe 3:** Una estocada o un tajo descendente más potente. Mayor daño, puede causar un breve *stagger* (interrupción) a enemigos pequeños. Ligera recuperación más larga.
    *   **Ventana de Combo:** Si el jugador espera demasiado entre pulsaciones, el combo se reinicia.
    *   **Coste de Stamina:** Cada golpe consume una pequeña cantidad de Stamina. El tercer golpe consume un poco más.

*   **Ataque Cargado:**
    *   **Activación:** Mantener presionado el botón de ataque principal.
    *   **Carga:** Aitor adopta una postura, acumulando energía en su espada (quizás con un efecto visual en el lauburu de la espada). La velocidad de movimiento se reduce durante la carga.
    *   **Ejecución:** Al soltar el botón, Aitor desata un potente tajo amplio o una estocada con mayor alcance.
    *   **Efectos:**
        *   Daño significativamente mayor que los ataques ligeros.
        *   Capacidad de romper la guardia de algunos enemigos o destruir escudos débiles.
        *   Mayor *stagger* o incluso derribo a enemigos medianos.
    *   **Coste de Stamina:** Consume una cantidad considerable de Stamina al ejecutarlo, proporcional al tiempo de carga (hasta un máximo).

### 2. Mecánicas Defensivas

*   **Bloqueo (Guardia):**
    *   **Activación:** Mantener presionado un botón de defensa (ej: `Click Derecho Ratón` / `Botón L1/LB Mando`).
    *   **Efecto:** Aitor levanta su espada para bloquear ataques frontales.
        *   Reduce un alto porcentaje del daño físico recibido (ej: 75-90%).
        *   No protege de ataques por la espalda, agarres, o ciertos ataques mágicos/elementales potentes (a menos que la espada esté imbuida).
    *   **Coste de Stamina:**
        *   Consumo pasivo de Stamina mientras se mantiene la guardia.
        *   Consumo adicional de Stamina al recibir un impacto bloqueado (mayor coste si el ataque es pesado).
        *   Si la Stamina se agota al recibir un golpe mientras se bloquea, la guardia de Aitor se rompe, dejándolo vulnerable por un instante (animación de *guard break*).

*   **Esquiva (Rodar/Dash):**
    *   **Activación:** Pulsar un botón de esquiva (ej: `Barra Espaciadora` / `Botón Círculo/B Mando`) + dirección opcional.
    *   **Efecto:** Aitor realiza un rápido movimiento evasivo (un rodar o un dash corto).
    *   **Invulnerabilidad (i-frames):** Proporciona un breve periodo de invulnerabilidad durante la parte inicial/media de la animación, permitiendo atravesar ataques si se sincroniza bien.
    *   **Coste de Stamina:** Consume una cantidad fija y moderada de Stamina por cada esquiva.
    *   **Cooldown:** No tiene un cooldown estricto, pero el uso repetido se ve limitado por la Stamina disponible.

*   **Parada (Parry):**
    *   **Activación:** Pulsar el botón de defensa justo antes de que un ataque enemigo conecte (ventana de tiempo ajustada).
    *   **Efecto Exitoso:**
        *   Desvía completamente el ataque físico enemigo.
        *   El enemigo queda desequilibrado o en estado de *stagger* durante un periodo más prolongado que un *stagger* normal.
        *   Abre una ventana para un **Contraataque (Riposte)**: una animación especial de ataque que inflige daño crítico.
        *   No consume Stamina; podría incluso restaurar una pequeña cantidad como recompensa por la habilidad.
    *   **Fallo:** Si se falla la sincronización, Aitor recibe el golpe (posiblemente con daño aumentado si estaba en mitad de una animación de intento de parry).
    *   **Feedback:** Requiere un claro feedback visual y sonoro para el éxito y el fallo.

## II. Resistencia (Stamina)

*   **Barra de Stamina:** Visible en la UI, debajo o cerca de la barra de salud.
*   **Consumo:**
    *   Ataques (ligeros, cargados).
    *   Esquivar.
    *   Mantener el bloqueo.
    *   Recibir daño mientras se bloquea.
    *   Correr (Sprint).
    *   Otras habilidades especiales que puedan añadirse.
*   **Regeneración:**
    *   La Stamina se regenera automáticamente a una velocidad constante cuando Aitor no está realizando acciones que la consuman o la pausen.
    *   La regeneración se detiene o es significativamente más lenta mientras se mantiene el bloqueo o se está corriendo.
*   **Agotamiento (Stamina Break):**
    *   Si la Stamina llega a cero, Aitor entra en un estado de "fatiga" breve.
    *   Durante la fatiga: no puede atacar, bloquear, esquivar ni correr. Su velocidad de movimiento se reduce.
    *   Debe esperar a que la Stamina se regenere hasta un umbral mínimo para volver a realizar acciones costosas.
    *   Este estado lo deja muy vulnerable.

## III. Magia Elemental (Aitor)

Aitor puede canalizar el poder de los cuatro elementos primarios: Fuego, Agua, Tierra y Aire. Inicialmente, podría tener acceso limitado, desbloqueando o mejorando sus afinidades elementales a medida que avanza en la historia o encuentra artefactos/conocimiento ancestral.

### 1. Recurso Mágico: "Adur" (Energía Espiritual/Mágica)

*   **Barra de Adur:** Una barra separada de la Salud y la Stamina, visible en la UI. Representa la energía espiritual o mágica de Aitor.
*   **Regeneración:**
    *   El Adur se regenera lentamente de forma pasiva.
    *   Podría haber consumibles (ej: "Edabeak" - pociones) o puntos de poder en el mapa (santuarios) que restauren Adur más rápidamente.
    *   Ciertas acciones (quizás paradas perfectas o derrotar enemigos de formas específicas) podrían otorgar pequeñas cantidades de Adur.
*   **Agotamiento:** Si el Adur se agota, Aitor no podrá lanzar hechizos hasta que se regenere una cantidad mínima. No implicaría una penalización de movimiento como el agotamiento de Stamina, pero sí una incapacidad mágica temporal.

### 2. Lanzamiento y Selección de Hechizos

*   **Selección Elemental:**
    *   **Rueda Elemental:** Mantener presionado un botón modificador de magia (ej: `Q` en teclado / `R1/RB Mando`) podría abrir una rueda de selección rápida con los cuatro elementos. Mover el stick/ratón y soltar seleccionaría el elemento activo.
    *   **Ciclo Rápido:** Un botón dedicado (ej: `Tab` / `D-pad Arriba/Abajo`) podría permitir ciclar rápidamente entre los elementos desbloqueados.
*   **Lanzamiento de Hechizos:**
    *   Un botón dedicado para lanzar el hechizo del elemento actualmente seleccionado (ej: `E` en teclado / `R2/RT Mando`).
    *   Algunos hechizos podrían tener una variante "cargada" si se mantiene el botón, consumiendo más Adur para un efecto mayor.
*   **Coste de Adur:** Cada hechizo consumirá una cantidad específica de Adur.
*   **Cooldowns:**
    *   En lugar de cooldowns individuales estrictos por hechizo, podríamos tener un breve cooldown global después de lanzar un hechizo para evitar el spam excesivo.
    *   Alternativamente, hechizos más poderosos podrían tener cooldowns individuales, mientras que los básicos solo se limitan por el Adur. (Mi preferencia inicial es limitar por Adur y un pequeño cooldown global para mantener el flujo).

### 3. Hechizos Elementales Básicos (Ejemplos Iniciales)

Aitor comenzaría con versiones básicas, que podrían mejorarse o evolucionar.

*   **Fuego (Sua):**
    *   **Proyectil de Fuego:** Lanza una bola de fuego que inflige daño y puede aplicar el estado "Quemado" (daño por tiempo leve).
    *   **Aliento de Fuego (Cargado):** Un cono de fuego de corto alcance que inflige daño continuo.
*   **Agua (Ura):**
    *   **Chorro de Agua:** Un proyectil de agua que inflige daño moderado y puede empujar ligeramente a enemigos pequeños o apagar fuegos.
    *   **Escudo de Agua (Cargado/Defensivo):** Crea una barrera temporal que reduce el daño de un golpe o apaga el estado "Quemado" en Aitor.
*   **Tierra (Lurra):**
    *   **Proyectil de Roca:** Lanza un trozo de roca que inflige daño físico y puede tener alto impacto (stagger).
    *   **Piel de Piedra (Cargado/Defensivo):** Aumenta temporalmente la defensa de Aitor, reduciendo el daño recibido.
*   **Aire (Haizea):**
    *   **Ráfaga de Viento:** Empuja a los enemigos hacia atrás, puede interrumpir ataques o desviar proyectiles débiles. No inflige mucho daño directo.
    *   **Salto Potenciado (Cargado/Utilidad):** Una ráfaga de viento bajo los pies que permite un salto más alto o más largo, útil para exploración y evasión.

### 4. Imbuir Espada (Lauburu Elemental)

El lauburu en la espada de Aitor es clave aquí.

*   **Activación:** Tras seleccionar un elemento, Aitor podría realizar una acción específica (ej: mantener el botón de magia y luego el de ataque, o un botón dedicado para imbuir) para canalizar ese elemento en su espada.
*   **Duración:** La imbuición duraría un tiempo limitado o un número específico de golpes.
*   **Coste:** Consumiría una cantidad significativa de Adur para activar.
*   **Efectos:**
    *   **Fuego:** Añade daño de fuego a los ataques de espada, puede aplicar "Quemado".
    *   **Agua:** Los ataques pueden ralentizar ligeramente a los enemigos o tener un efecto "limpiador" contra ciertas defensas.
    *   **Tierra:** Aumenta el daño de impacto/stagger de los ataques de espada, puede romper guardias más fácilmente.
    *   **Aire:** Aumenta la velocidad de ataque de la espada ligeramente, los golpes pueden empujar un poco más.
*   **Sinergia:** Imbuir la espada podría ser la forma de dañar efectivamente a ciertos enemigos con resistencias elementales específicas o de explotar sus debilidades.

### 5. Interacciones Elementales

Considerar interacciones básicas entre elementos podría añadir profundidad:
*   Agua apaga Fuego (tanto en el entorno como en enemigos quemados).
*   Fuego puede prender superficies aceitosas o secar áreas mojadas.
*   Tierra mojada podría crear barro que ralentice.
*   Aire podría avivar el fuego o dispersar nubes de gas/agua.

---
**Próximos Pasos:**
1.  ~~Diseñar un arquetipo de enemigo básico para probar estas mecánicas de combate y magia.~~ (Completado)
2.  ~~Detallar el sistema de progresión de Aitor (cómo mejora habilidades, desbloquea hechizos, estadísticas, etc.).~~ (En progreso)
3.  Explorar el diseño de los otros personajes jugables y sus roles (Mari, Sugaar, Basajaun, Lamia) para el modo historia y competitivo.
4.  Considerar la IA básica para el "Gaizto Kume" y otros enemigos iniciales.
5.  Esbozar el sistema de Puzzles basados en símbolos vascos.

## V. Sistema de Progresión de Aitor

La progresión de Aitor se centrará en el descubrimiento, el dominio de sus habilidades ancestrales y la conexión con el mundo que lo rodea. No se basará en un sistema de "niveles" tradicional con puntos de experiencia por matar enemigos, sino en hitos de la historia, exploración y superación de desafíos específicos.

### 1. Mejora de Estadísticas Base (Salud, Stamina, Adur)

*   **Fragmentos de Lauburu / Bendiciones Ancestrales:**
    *   Aitor podrá encontrar "Fragmentos de Lauburu" escondidos en el mundo (cofres, recompensas de puzzles, áreas secretas) o recibir "Bendiciones Ancestrales" al completar misiones importantes o ayudar a ciertos personajes.
    *   Cada cierto número de fragmentos recolectados (ej: 3 o 4), o al recibir una bendición, el jugador podrá elegir aumentar permanentemente una de sus estadísticas base:
        *   **Corazón (Bihotza):** Aumenta la Salud máxima.
        *   **Aliento (Arnasa):** Aumenta la Stamina máxima.
        *   **Espíritu (Izpiritua):** Aumenta el Adur máximo.
    *   Esto permite al jugador especializar ligeramente a Aitor según su estilo de juego.
*   **Equipo y Amuletos:**
    *   Aunque no se centre en un looteo constante, Aitor podría encontrar o fabricar piezas de equipo (ej: brazales, grebas, talismanes) que ofrezcan pequeñas mejoras a estas estadísticas o resistencias elementales. Estos serían hallazgos significativos, no caídas comunes.

### 2. Desbloqueo y Mejora de Habilidades de Combate y Magia

*   **Santuarios Olvidados / Estelas con Inscripciones:**
    *   Nuevos hechizos elementales, variantes de hechizos existentes (ej: el `Aliento de Fuego` como mejora del `Proyectil de Fuego` o un hechizo distinto), o nuevas técnicas de espada (ej: un nuevo remate para el combo, una mejora para el parry) se desbloquearían al interactuar con santuarios dedicados a los elementos o a antiguos guerreros vascos, o al descifrar estelas con inscripciones rúnicas.
    *   Estos puntos de aprendizaje estarían ligados a la exploración y a la superación de desafíos (a veces protegidos por enemigos o puzzles).
*   **Recuerdos Desencadenados:**
    *   Dado que Aitor ha perdido la memoria, ciertos eventos clave de la historia, interacciones con aliados, o la visita a lugares significativos de su pasado (que irá descubriendo) podrían desencadenar "Recuerdos".
    *   Estos recuerdos no solo avanzarían la trama, sino que también podrían desbloquear o potenciar habilidades específicas, representando el conocimiento que resurge en él. Por ejemplo, recordar un entrenamiento con su mentor podría mejorar la efectividad de su parada o desbloquear un nuevo combo.
*   **"Eskuak" (Manos) - Puntos de Habilidad Elemental:**
    *   Al interactuar con fuentes de poder elemental o al derrotar a jefes mitológicos ligados a un elemento, Aitor podría obtener "Eskuak" de ese elemento (Mano de Fuego, Mano de Agua, etc.).
    *   Estos "Eskuak" podrían gastarse en un menú de habilidades sencillo y temático (quizás un árbol estilizado como un roble o un lauburu) para mejorar aspectos específicos de sus hechizos elementales o imbuiciones:
        *   **Fuego:** Mayor daño, mayor duración del quemado, menor coste de Adur.
        *   **Agua:** Mayor efecto de empuje/ralentización, mayor duración del escudo, curación adicional al usar `Escudo de Agua`.
        *   **Tierra:** Mayor reducción de daño de `Piel de Piedra`, mayor impacto de `Proyectil de Roca`, mayor duración de la imbuición de tierra.
        *   **Aire:** Mayor alcance de `Ráfaga de Viento`, mayor altura/distancia del `Salto Potenciado`, menor coste de Adur para hechizos de aire.
    *   Esto permitiría una especialización elemental más profunda si el jugador lo desea.

### 3. Progresión Narrativa y Desbloqueo de Aliados

*   **Avance en la Historia:** El principal motor de progresión será la historia. Descubrir nuevas áreas, conocer nuevos personajes y avanzar en la trama desbloqueará naturalmente nuevas oportunidades y desafíos.
*   **Reunir Aliados:** Como se menciona en la historia, Aitor reunirá aliados. Estos aliados no solo serían personajes jugables en el modo competitivo, sino que en el modo historia podrían:
    *   Ofrecer misiones secundarias que recompensen con mejoras o conocimientos.
    *   Enseñar a Aitor habilidades pasivas o activas únicas (ej: Mari podría enseñarle a Aitor una forma de potenciar sus hechizos de tormenta si Aitor tiene afinidad con el aire, o Basajaun podría enseñarle a moverse más sigilosamente por los bosques).
    *   Acompañarlo en ciertas secciones como NPCs de apoyo con sus propias habilidades.

### 4. "Lauburuaren Bidea" (El Camino del Lauburu) - Diario de Progresión

*   Aitor podría tener un diario o un menú de "El Camino del Lauburu" donde se registren:
    *   Sus recuerdos recuperados.
    *   Las habilidades aprendidas y cómo mejorarlas.
    *   Pistas sobre santuarios o estelas por descubrir.
    *   Información sobre las criaturas mitológicas y sus debilidades (una vez descubiertas).
    *   El progreso de sus misiones principales y secundarias.
    *   Esto serviría como guía para el jugador y como un recordatorio de su viaje y crecimiento.

## IV. Arquetipo de Enemigo Básico: Gaizto Kume (Cachorro Maligno)

El Gaizto Kume es un enemigo común de bajo nivel diseñado para que el jugador practique las mecánicas fundamentales de combate.

### 1. Descripción y Comportamiento

*   **Apariencia:** Criaturas pequeñas y ágiles, de aspecto feral o ligeramente corrompido. Podrían ser humanoides encorvados con garras rudimentarias o portando armas improvisadas (palos afilados, piedras). Se mueven de forma errática.
*   **Comportamiento General:**
    *   Agresivos cuando detectan a Aitor, especialmente en grupos.
    *   Tienden a atacar con embestidas rápidas y golpes sencillos.
    *   Pueden intentar rodear al jugador si están en número suficiente.
    *   Si están solos y con poca salud, podrían intentar huir brevemente antes de reagruparse o ser presa del pánico.
*   **Salud:** Baja. Deberían caer con un combo completo de Aitor, un ataque cargado bien colocado, o unos pocos hechizos básicos.
*   **Daño:** Bajo. Su amenaza principal radica en su número y su capacidad para interrumpir las acciones del jugador si no se manejan con cuidado.

### 2. Habilidades del Gaizto Kume

*   **Zarpazo Rápido / Golpe Salvaje:**
    *   Un ataque cuerpo a cuerpo rápido y con poco alcance.
    *   **Telegrafiado:** Un breve gruñido o un ligero retroceso antes de lanzarse.
    *   **Interacción con Aitor:** Puede ser bloqueado, esquivado o parado. Si Aitor lo para, el Gaizto Kume quedará muy vulnerable.
*   **Embestida Corta:**
    *   El Gaizto Kume se lanza hacia adelante una corta distancia para cerrar el espacio y atacar.
    *   **Telegrafiado:** Una postura más baja y un sonido distintivo antes de la embestida.
    *   **Interacción con Aitor:** Puede ser esquivado lateralmente. Si se bloquea, podría consumir una cantidad notable de Stamina de Aitor o incluso empujarlo ligeramente si no está bien posicionado. Un ataque cargado de Aitor podría interrumpir la embestida si se sincroniza bien.

### 3. Vulnerabilidades y Resistencias

*   **Vulnerabilidad al Stagger:** Son fácilmente interrumpidos (staggered) por los ataques de Aitor, especialmente el tercer golpe del combo ligero, los ataques cargados, o hechizos de impacto como `Proyectil de Roca`.
*   **Resistencias Elementales:** Ninguna resistencia particular. Reciben daño normal de todos los elementos. Esto los hace ideales para que el jugador experimente con sus diferentes hechizos e imbuiciones de espada.
*   **Debilidad al Control de Masas Ligero:** Hechizos como `Ráfaga de Viento` pueden dispersarlos o interrumpirlos fácilmente. `Chorro de Agua` también podría empujarlos.

### 4. Propósito en el Diseño del Juego

*   **Tutorial Viviente:** Sirven para enseñar al jugador las mecánicas básicas de ataque, defensa (bloqueo, esquiva, parada), y gestión de Stamina.
*   **Prueba de Magia Inicial:** Permiten al jugador probar el efecto de sus primeros hechizos elementales y la mecánica de imbuir la espada sin demasiada presión.
*   **Fomentar la Agresividad Controlada:** Su baja salud y vulnerabilidad al stagger recompensan al jugador por ser proactivo, pero su número puede castigar la imprudencia.
*   **Feedback Inmediato:** Las reacciones del Gaizto Kume a las acciones de Aitor (ser parado, empujado por magia, etc.) deben ser claras y satisfactorias.