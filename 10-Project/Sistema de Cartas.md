---
tags: [project, cards, mcp, design-system]
scope: out-of-ontology
updated: 2026-07-30
---

# Sistema de cartas — tipos y decisiones

Registro durable de decisiones de presentación y software tomadas durante los proyectos de Tarot Club e inside jokes. No es fuente de evidencia sobre la novela. El copy factual sigue saliendo de `02-Wiki/` y sus enlaces directos a `01-Sources/`.

## Familias disponibles

El estudio admite trece tipos:

1. `Character`
2. `Artifact`
3. `Cover`
4. `Full Image Cover`
5. `Tier`
6. `Pathway`
7. `Tier Explanation`
8. `General Explanation`
9. `Pathway Explanation`
10. `Breakdown`
11. `Map`
12. `Tarot Member`
13. `Corruption File`

Límites de campos, criterios de selección y flujo MCP: [[Card MCP Usage Guide]].

## LOTM — Every Tarot Club Member Explained

- `Tarot Member` es una familia de análisis de personajes, no otra carta de estadísticas.
- Conserva tres composiciones: `Portrait`, `Dossier` y `Contrast`. El conjunto no debe parecer una única plantilla repetida.
- Klein Moretti debe existir como miembro desde el comienzo del proyecto.
- Audrey, Xio, Derrick, Emlyn y los demás miembros usan copy irónico y juguetón antes que prosa solemne de enciclopedia.
- Chiste de Derrick: el día más apocalíptico de cualquier otro miembro sería un martes cualquiera en la Ciudad de Plata.
- Investigación comunitaria puede orientar tono, pero el copy final de Xio y las demás cartas es autocontenido y no menciona Reddit ni plataformas externas.
- Selector explícito de color: aporta variedad e identidad visual, pero no afirma que el color sea canon.
- Layout condicionado por contenido: nombres, descripciones y textos secundarios largos activan densidad; contenido corto no crea desiertos verticales artificiales.

## LOTM — Inside Jokes Explained

- `Corruption File` existe porque este proyecto necesitaba una identidad claramente distinta de los expedientes de Tarot Club.
- Dirección visual: pósteres ruidosos de autopsia de memes, avisos de peligro, archivos de evidencia y colapso de contexto; no tarot ornamental.
- Copy divertido, irónico y jocoso, pero comprensible sin publicaciones, citas comunitarias ni plataformas externas.
- Tres composiciones: `Warning`, `Evidence` y `Quote`.
- `Evidence` responde a longitud del título: incidentes largos apilan explicación y reacción en lugar de forzar columnas estrechas.
- Imágenes de fondo soportadas en editor, preview interactivo, renderer estático, ZIP y vídeo.
- Opacidad de imagen y opacidad del velo son propiedades separadas. Evita que Dark Reader convierta el velo en capa opaca y esconda la imagen.
- Número de incidente opcional: UI muestra `Hidden / Visible`; MCP expone `showIncidentNumber`; valor predeterminado `false`.
- Cuando se muestra, número deriva de longitud del título y se rellena a cuatro dígitos. Es decoración sin significado narrativo, cronológico o canónico.

## Reglas de layout

- Diseño base fijo: 480×640. Exportación PNG: 960×1280.
- Layout sigue condiciones de contenido, no zonas vacías fijas. Contenido denso reduce o apila; contenido escaso compacta.
- Notas al pie permanecen asociadas al cuerpo. No se fijan lejos de contenido corto solo para llenar altura.
- Títulos largos usan clases de tamaño y wrapping seguro. Ninguno puede salir de la carta.
- Arte de fondo queda subordinado al texto. Slider controla visibilidad; velo mantiene legibilidad.
- `Tarot Member` y `Corruption File` pueden compartir infraestructura, nunca lenguaje visual.

## Reglas de copy

- Voz divertida, irónica, juguetona y concisa antes que grandiosa.
- Humor nace de mecanismo, personalidad, consecuencia o contraste real de LOTM.
- Copy final no cita Reddit, posts, sitios web ni proceso de investigación.
- Una broma fuerte por carta. Texto secundario escala o contradice; no repite.
- Footnotes innecesarias funcionan como remate, no contenedor de overflow.
- Límites de precisión sobreviven al chiste: interpretación, teoría, acceso condicional y alcance de Pathway mantienen sus etiquetas.

## Imágenes, ZIP y vídeo

- Imágenes subidas se guardan como archivos. JSON conserva solo URL `http(s)` o ruta del sitio.
- Editor y MCP comparten misma biblioteca SQLite.
- ZIP renderiza todos los tipos, no solo portadas. Incluye PNG y manifiesto.
- Vídeo usa mismo renderer estático para coincidir con PNG.
- Cada carta puede tener duración propia; MP4 respeta esas duraciones.
- Tipo nuevo queda incompleto hasta funcionar en schema, estado del editor, ambos previews, renderer estático, MCP, ZIP y vídeo.

## Contrato MCP

- Nombre de producción: `lotm-card-studio`.
- Versión tras soporte de número opcional: `1.3.0`.
- `Corruption File.showIncidentNumber`: booleano, valor predeterminado `false`.
- `save_card_batch` crea; `update_card` modifica contenido sin cambiar posición o sección.
- Descripciones del schema deben exponer opciones visuales. Cliente MCP no debe inferir comportamiento oculto de UI.
- Tras cambiar schema: reiniciar servicio MCP y reconectar clientes para refrescar herramientas cacheadas.

## Verificación registrada

- Suite completa tras número opcional: 271 pruebas aprobadas.
- Pruebas focalizadas cubren schema, MCP y render con número oculto y visible.
- Commits de producción: `3d830b1` para comportamiento y `48992c5` para actualización del contrato MCP en `lotm-game`.
- Cartas existentes mantienen número oculto salvo `showIncidentNumber: true` explícito.

## Mantenimiento

Actualizar esta nota cuando cambie un tipo, composición, regla compartida de imagen, condición de densidad, ruta de exportación u opción visible por MCP. Chat no es especificación durable.
