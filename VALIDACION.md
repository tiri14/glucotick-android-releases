# Validación de la beta 0.1.14-beta.1

**Beta validada localmente el28/10/2026, con los APK de producción y su firma permanente.** Incluye móvil0.1.14, Wear OS0.1.6 y cinco esferas. Sigue siendo una beta: las pruebas físicas con esta firma y la autonomía prolongada están pendientes.

| Comprobación local | Resultado actual |
|---|---|
| Siete APK de producción | Firma común, versiones y mínimos contrastados; no depurables, sin integración Android Auto ni fixtures de pruebas |
| Pruebas unitarias |87 aprobadas sobre la compilación Release |
| Android8/API26 y Android16/API36 |26 regresiones por emulador y pruebas de instalación/actualización aprobadas; cuenta ficticia cifrada y widget conservados |
| Wear API33 y API36 |9 regresiones por emulador e instalación/actualización con conservación de estado aprobadas |
| Cinco esferas WFF |Validación oficial del formato aprobada; esto no certifica por sí solo el funcionamiento visual |
| Presentación nativa |Cinco esferas finales en Wear36 en activo/AOD: reciente, gris, tachada, oculta y unidades. Dúo Radial también en Wear33, con tendencia corregida, HI/LO, datos ausentes y cinco franjas.80 capturas revisadas; Original comprobada durante65s de AOD |
| Caducidad sin recibir otra lectura |Cruces naturales de5/15/60min observados en AOD Wear36; cambia a gris, tachado y ocultación conservando la fecha original. La cadencia visual la controla el renderizador del reloj |
| Pérdida y retorno de red |Prueba real por Android26/36: conserva fechas originales, muestra error de red y mantiene la parada voluntaria al recuperarse la conexión. Solo datos ficticios; no sustituye una cuenta LibreLinkUp real |
| Paquete e instalador |Instalación, actualización y rechazos comprobados en entornos aislados. El ZIP incorpora manifiesto y sumas para verificar también guías e imágenes mediante VerifyOnly |
| Enlace móvil–reloj con firma pública |6 escenarios aprobados en una pareja oficial de emuladores API36: envío/recepción, ACK, pérdida completa de túnel y redes, recuperación y resincronización. ACK nuevo de la revisión recuperada, sin renovar la fecha de medición ni de consulta de origen. Refresco de Original tras recepción real contrastado |

Fuente de los APK empaquetados: `ac152efde6578fbb92cd682e0595074197d10fd1`. Certificado SHA-256: `7f769c9fcf09e2b5333e729259b6359e0cd03565ae84f4e9e8dbbae514cb1478`. Las pruebas se ejecutan localmente; no hay CI de GitHub ejecutado para esta beta. Los resultados fallidos de preparación se conservan en privado, incluidos los ajustes de instrumentación; no se cuentan como aprobaciones ni sustituyen las ejecuciones sobre la candidata final. El enlace se prueba con lecturas ficticias, servicios de Google y acompañante oficial, sin sustituir el APK de producción por uno de pruebas.

El renderizador Google332010000 inicial del SDK rechazó Dúo Radial durante la preparación anterior. La candidata actual se comprueba en API33 con el renderizador oficial334200060, mínimo API33 y misma firma Google, y se activa correctamente. No se vuelve a certificar el renderizador anterior con esta candidata. Mantén actualizados el sistema y sus servicios. Este resultado no certifica todas las versiones de renderizador de cada fabricante.

Las instalaciones privadas del entorno personal de desarrollo se conservaron durante estas pruebas; no se valida una migración de firma. Pruebas físicas de la firma pública y autonomía prolongada permanecen pendientes. Los resultados históricos de instalaciones privadas no se cuentan como pruebas nuevas de producción.
