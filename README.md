# Expediente QC: las piezas que se deshacen · Experiencia concreta (EC)

Guía para el docente. Unidad didáctica **Producción y publicación de piezas gráficas** · Mg. Mario Quiroz Martinez.

## Justificación DUA-Experiencial

La actividad adopta el enfoque **DUA-Experiencial**: ofrece múltiples formas de implicación, representación y acción/expresión, y organiza el aprendizaje en experiencia concreta, reflexión guiada, conceptualización y aplicación. La sesión se centra en la **Experiencia concreta (EC)**: el estudiante manipula las piezas defectuosas y reproduce la falla antes de recibir cualquier definición; el resto del ciclo se recorre de forma breve para cerrar la experiencia.

| Estación | Fase | Mecánica | Puntaje |
| --- | --- | --- | --- |
| Enigma 1 · La devolución | EC | Manipular piezas (estirar, lavar, aplicar fuerza, lupa) · registro de observaciones · hipótesis previa | 25 |
| Lista de verificación | EC → OR | Compuerta de 3 ítems | — |
| Enigma 2 · El archivador | OR · CA | Candado deductivo (clave 160) · definición por contraste · emparejamiento concepto–evidencia | 40 |
| Enigma 3 · Reproduce la falla | EC · EA | Simuladores de prensa DTF e impresora 3D (4 misiones) · cálculo de desviaciones | 35 |
| Ficha técnica | OR | Verdadero o falso razonado (5) | 20 |
| Video de apoyo · El archivo DTF por dentro | CA | Video de YouTube con capítulos y saltos · 8 preguntas sobre la preparación del archivo DTF · 1 pregunta puente: defecto de archivo vs. defecto de proceso | 50 |
| Enigma 4 · Anagramas | CA | DELAMINACIÓN · CURADO · INTERCAPA | 30 |
| Enigma final · Caja fuerte | EA | Combinación 30·10·35 · 2 casos de transferencia · contraste de hipótesis · reflexión y ticket | 50 |
| **Total** | | | **250** |

**Video de apoyo:** [«Canal Blanco en DTF: Todo lo que Debes Saber»](https://www.youtube.com/watch?v=h231tfjdSyw). Está siempre disponible desde el botón 🎬 Video de la barra superior, con capítulos y un resumen escrito por capítulo (no se reproduce la transcripción). Las preguntas se basan solo en lo que dice el video: canal blanco como base, 300 ppp y CMYK, contraer la selección 1 px, canal de tinta plana `spot_white` en color negro, orden de impresión CMYK → blanco, formato TIF, por qué se reduce el blanco (borde no deseado) y diseño 100 % blanco sin contraer. Desde el servidor del curso el video se ve dentro de la página; abierta como archivo local, ofrece abrirlo en YouTube en el minuto exacto.

- **Implicación:** narrativa de misterio, enigmas con candado, insignias, misiones y error productivo sin castigo (paneles Pista · Dato clave · Contexto).
- **Representación:** piezas ilustradas que reaccionan, reporte tabular, escalas con objetivo y medido, vista microscópica, corte de capas, mapa del proceso y glosario.
- **Acción y expresión:** manipular controles, seleccionar, emparejar, calcular, anagrama por fichas o teclado, escribir y autoevaluarse.

## Fidelidad a la fuente

Todos los valores técnicos provienen del reporte del caso:

- **DTF:** objetivo 160 °C / 20 s con presión neumática uniforme; medido 130 °C / 10 s; fusión del TPU entre 150 y 170 °C.
- **3D:** objetivo 210 °C; medido 175 °C.

**Artes finales del Enigma 1:** la camiseta de la Evidencia A usa dos artes finales reales del pedido, `078yp2qo.cdr` (águila ornamental, monocromo) y `r7vm6967.cdr` (calavera «Youth Crew», a color), exportados desde CorelDRAW con Inkscape 1.4 e incrustados en WebP de 640 px. El estudiante debe revisar los dos diseños antes de registrar su observación: el mismo defecto aparece en ambos, lo que aporta evidencia contra la hipótesis «es el diseño del archivo».

**Llavero 3D de la Evidencia B:** es la cabeza de Lilica (`lilica_SubTool4.stl`, modelo de gilafonso), aligerada de 95 601 a 26 000 triángulos e incrustada en la página (cuantizada y comprimida, unos 290 KB). Se dibuja con WebGL2 sin librerías externas: tiene capas de 0,75 mm (exageradas para que se vean), un ojal impreso en el cráneo y una argolla metálica. Al aplicar fuerza se rompe en la unión entre las capas 22 y 23, bajo el ojal: las orejas quedan colgadas de la argolla y la cabeza cae mostrando la cara de fractura. Se puede girar arrastrando o con las flechas del teclado, y la lupa acerca la cámara a la zona de fractura. Si el navegador no tiene WebGL2, se muestra el llavero SVG original.

Los simuladores no inventan consecuencias para valores que el reporte no documenta: los marcan como *fuera de especificación / no validado*. La narrativa (devolución del cliente, nota del supervisor, casos nuevos de bolsas tote y figura 3D) es ficción didáctica.

## Evidencia y datos

- Informe en **PDF y MD** con cada respuesta, sus intentos y sus puntos; observaciones, hipótesis, desviaciones, registro del simulador, verdadero o falso y reflexiones.
- Las respuestas se guardan en el navegador del estudiante (`localStorage`, clave `expediente-qc-merch-registro-v1`) y se pueden retomar.
- El PDF se genera con jsPDF 2.5.1 y jsPDF-AutoTable 3.8.2 incrustados: funciona sin conexión.
- Desde el servidor del curso carga `/envio-resultados.js` con `data-sub="ec"` y envía el avance al panel docente.
