---
tags: [project, legal, risk]
scope: out-of-ontology
updated: 2026-07-30
---

# IP y Riesgo Legal — Archivo de Misterios

Ver [[README]]: esta nota no sigue el modelo epistémico de `AGENTS.md`. Es un registro de riesgo de negocio, no una afirmación sobre el canon de la novela.

## Estructura real de derechos (investigado 2026-07-30)

- **China Literature Ltd. (Tencent / Qidian)** — dueño de los derechos originales en chino; publicó la versión impresa china en 2020.
- **Webnovel** (rama inglesa de Qidian) — traducción oficial online en inglés.
- **Yen Press** — derechos de impresión en inglés (primer volumen físico, julio 2025).
- **SPARK NEXA** — desarrollador/publisher del MMORPG oficial licenciado.

## Fecha ancla: 21 de agosto de 2026

El MMORPG oficial (Unreal Engine 5, SPARK NEXA) lanza en China (PC/Android/iOS) ese día; lanzamiento global (inglés/japonés/coreano) más adelante en 2026. Es un juego de **acción en tercera persona en tiempo real** (combate, clases tank/DPS/support, PvP) — producto de forma radicalmente distinta a un juego web de combinación de conceptos.

**Matiz importante:** el propio sistema de progresión del MMORPG usa una submecánica de "preparar pociones de secuencia combinando fórmulas e ingredientes" — hay cierto solapamiento conceptual con el juego, aunque envuelto en un producto de combate totalmente distinto. La mecánica de Archivo de Misterios es "combinar **conceptos** abstractos" (estilo Little Alchemy clásico), no "combinar ingredientes para craftear pociones" — esto reduce el solapamiento real, aunque las mecánicas de combinación en general no suelen ser objeto de propiedad intelectual protegible de todas formas.

**Por qué importa la fecha:** antes del 21 de agosto no hay producto oficial de juego que "proteger" comercialmente en este espacio. Después, sí lo hay, con un titular de derechos activo (Tencent/SPARK NEXA) con presupuesto de marketing vigilando el mismo espacio de búsqueda.

## Evidencia sobre tolerancia a fan-works

- **No se encontró ningún pleito ni cese-y-desista documentado** contra ningún fan-work de LOTM. Ausencia notable, pero no es prueba definitiva de tolerancia.
- **Postura histórica de Qidian/China Literature hacia fan-translators:** de reconocimiento y búsqueda de cooperación (ofrecieron convertir traductores de fans en socios formales), no de persecución legal agresiva. Evidencia indirecta (sobre traducciones, no juegos).
- **Fan-game existente confirmado:** "Lord of Mystery" de David Fang en itch.io — juego de cartas lovecraftiano "inspirado en" LOTM (tarot, ocultismo, Beyonders), con página de compra activa. No se confirmó si usa nombres exactos de personajes. Es la evidencia más concreta de que fan-games de LOTM operan y monetizan sin acción legal aparente — pero es un solo punto de datos, de baja visibilidad, no prueba nada a la escala que busca este proyecto.

## Distinción de riesgo que se estableció

- **Riesgo legal formal** (demanda del titular de derechos) — lento, caro, poco común.
- **Riesgo de plataforma/takedown** (DMCA o reporte de ToS en TikTok, itch.io, o el procesador de pago) — barato, rápido, y la vía real por la que la mayoría de fan-games desaparecen. "No hay pleitos documentados" no dice nada sobre este segundo riesgo, que es el que de verdad aplica a un proyecto de este tamaño.
- Patrón histórico observado en otros fan-games de IP asiática (AM2R, Pokémon Uranium): la tolerancia suele desplomarse **justo cuando lanza el producto oficial licenciado** — no antes. Refuerza la relevancia del 21 de agosto.

## Procesadores de pago (investigado 2026-07-30)

- **Patreon** prohíbe explícitamente monetizar contenido de IP no autorizada — caso real documentado de un fan-game con su cuenta de Patreon cerrada por esto exacto. Contradice la idea de que "Patreon es más seguro que IAP": no lo es, solo aplica la misma regla en otro punto.
- **Stripe** y **PayPal** tienen la misma prohibición explícita en sus políticas de uso aceptable, con procesos de reporte de infracción de IP para que el titular de derechos reclame.
- **Ko-fi / Buy Me a Coffee** procesan por debajo vía Stripe/PayPal — heredan la misma restricción.
- **Liberapay / Open Collective** son estructuralmente distintos (sin fines de lucro / transparencia financiera total) y se prestan a un encuadre de "financiar el proyecto" en vez de "comprar un producto" — reduce la superficie visible de lo que parece transacción comercial de mercancía con nombres protegidos, aunque la prohibición contractual de fondo sea similar.
- **Conclusión:** ningún procesador de pago da un escudo legal real — todos prohíben lo mismo en sus términos. La diferencia está en cuánta superficie expones y si alguien reporta.

## Mitigación ya implementada (no solo recomendada)

Ver [[Arquitectura del Juego]] para el detalle técnico. Resumen: arquitectura de datos desacoplada (nombres de LOTM solo como datos en Postgres, nunca en el modelo/lógica) + nombre de producto propio ("Archivo de Misterios") ya en uso en toda la interfaz. Esto no es un escudo legal (un cese-y-desista audita lo que el usuario final ve, no el schema de la base de datos) — es una ventaja operativa: permite reemplazar nombres rápido si hace falta reaccionar a un aviso de retiro.

## Veredicto real del abogado (2026-07-30)

Consultado un abogado de IP real (por fin, tras siete sesiones de consejo pidiéndolo). Veredicto: **el proyecto es legalmente delicado** por dos razones concretas:

1. Se planea usar **nombres canónicos exactos** de la novela (personajes, Secuencias, Rutas de Beyonder reales), no genéricos.
2. Es una **IP activa**, no dormida — donghua oficial licenciado + MMORPG de Tencent en camino (21 de agosto de 2026).

**Hallazgo que conecta esto con la prueba de usuarios:** los mismos dos términos que el abogado señala como el riesgo concreto ("Secuencia", conceptos de "Misticismo") son exactamente donde los 10 testers ajenos a LOTM se perdieron durante la prueba de valor. Ver [[Estrategia de TikTok y Validación]] para el detalle de esa prueba. El consejo (ronda 8, revisión cruzada 5/5) concluyó que es más defendible leer esto como **la misma fricción vista desde dos ángulos** (dependencia de vocabulario canónico) que como dos problemas independientes — aunque no es prueba definitiva, porque es casi tautológico que lo más canónico sea también lo menos familiar para un extraño.

**Costo nuevo identificado:** genericar "Secuencia"/"Misticismo" resolvería el riesgo legal y la confusión de usuarios, pero esos mismos términos son el gancho de descubrimiento orgánico (lo que buscan los fans de LOTM en TikTok/Google). Nadie había cuantificado ese costo antes.

**Matiz de alcance:** renombrar términos no blinda si la estructura general del sistema (progresión por niveles, jerarquía de rutas, combinar poderes) sigue siendo reconocible como copia — el riesgo puede estar en el "total look and feel", no solo en los nombres propios. Esto todavía no se le preguntó al abogado explícitamente.

## Replanteamiento (2026-07-30, ronda 9): NO genericar los nombres — con reservas

El usuario rechazó la recomendación de genericar "Secuencia"/"Misticismo", argumentando que perdería el gancho con la fanbase de LOTM y el apoyo del público de TikTok. El consejo revisó la decisión y llegó a una postura distinta a la de la ronda 8, con razones propias:

- **Los dos hallazgos (riesgo legal + confusión de testers) son problemas independientes**, no la misma causa: el riesgo legal viene de activos protegidos (nombres propios, facciones, tramas específicas), no de que "Secuencia"/"Misticismo" sean difíciles de entender. Renombrar esas dos palabras no reduce el riesgo legal si el resto del juego sigue siendo reconocible como LOTM. La confusión de los testers se resuelve con tutorial/glosario, no borrando términos.
- Por eso, **mantener los nombres canónicos no impide resolver ninguno de los dos problemas reales** por separado.
- **Rechazado explícitamente:** la idea de crecer rápido/grande antes del 21 de agosto para "ser políticamente costoso de tocar" — invierte la lógica real (más visibilidad = más riesgo de detección, no menos).

**Advertencia que el propio consejo se hizo a sí mismo (unánime, 5/5 en la revisión cruzada):** este giro de 180° llegó justo después de la objeción fuerte del usuario. El razonamiento se sostiene por mérito propio, pero ningún asesor se preguntó "¿estamos razonando o cediendo a lo que el usuario quiere oír?" antes de llegar ahí. Vale la pena tenerlo presente como sesgo posible, no solo como veredicto final.

**Dos huecos de información sin resolver:**
- Nadie tiene la cita textual del abogado — todo el análisis trabaja sobre la paráfrasis "delicado", no sobre lo que dijo exactamente.
- Nadie verificó si es cierto que cambiar esas dos palabras "pierde todo el gancho" — es una afirmación razonable pero no medida (¿cuánto del interés en el canal depende del vocabulario exacto de LOTM vs. de los personajes/trama/arte del contenido?).

## Acciones pendientes (actualizado)

1. ~~Consultar a un abogado de propiedad intelectual/entretenimiento real~~ — **hecho, 2026-07-30**. Ver veredicto arriba.
2. ~~Probar el juego con gente ajena a LOTM~~ — **hecho parcialmente, 2026-07-30** (10 personas, resultado cualitativo). Sigue pendiente definir el criterio numérico de éxito antes de la próxima prueba.
3. **Volver al abogado con una pregunta cerrada** (no "¿es delicado?"): lista específica de qué activos son alto riesgo (nombres propios, facciones, tramas) versus qué términos de mecánica genérica de género ("Secuencia", "Misticismo") son bajo riesgo por sí solos; y si la estructura general del sistema (progresión, rutas, jerarquía), más allá del vocabulario, sigue siendo el riesgo real. Esto es lo más urgente pendiente — casi todo lo demás depende de esta respuesta siendo más específica.
4. **Preguntarle al abogado por precedentes reales** (¿ha perseguido este titular a otros fan-works de LOTM?) y por la viabilidad de pedir una licencia/permiso directo en vez de solo evadir el riesgo.
5. **NO genericar los nombres por ahora** (decisión revertida en ronda 9) — en su lugar, arreglar la confusión de testers con tutorial/glosario, y mantener la arquitectura desacoplada lista para un swap rápido de nombres SI llega un cese-y-desista real (hedge técnico, no cambio permanente).
6. **Verificar con datos** cuánto del interés actual en el canal/juego depende del vocabulario exacto de LOTM vs. de otros elementos (personajes, trama, arte) — sigue sin medirse.
7. Monitorear el fan-game de itch.io como canario y escribir el plan de contingencia — seguían pendientes antes de esta ronda, no confirmado que se hayan resuelto.
8. Revisar toda la decisión el 21 de agosto de 2026 con los datos que existan para entonces.
