# heat-es-Mapa-de-calor-de-delitos-y-riesgo-urbano-en-Espa-a
HeatEs es un mapa sencillo y directo que muestra zonas con mayor concentración de señales de riesgo en España, de forma agregada y anónima.
No verás casos individuales, ni tipos de delito, ni direcciones. Solo un mapa de calor por zonas y por periodo.

Objetivo: informar y prevenir sin exponer a nadie ni alimentar el morbo.

Qué ves en la app

Mapa base gris neutro (limpio, sin distracciones).

Capa de calor que se adapta al zoom con calidad alta (no es una imagen borrosa; el calor se recalcula por niveles).

Ventanas temporales: 1 día, 1 mes, 1 año.

Nada más. Sin paneles complejos ni listas de incidentes.

Privacidad (lo importante)

Sin puntos exactos y sin tipos de incidentes visibles.

Agregación espacial mediante celdas H3: piensa en una rejilla hexagonal que resume la señal por zona.

Umbrales para evitar que una celda con muy pocos eventos destaque por sí sola.

La app muestra solo el agregado, no información individual ni identificable.

De dónde salen los datos

Fuentes abiertas y señales comunitarias moderadas.

Integración automática: procesos que recogen, normalizan y geocodifican datos de sitios públicos.

En la app solo aparece el resultado agregado, con decaimiento temporal (lo reciente pesa más).

La lista detallada de fuentes y metodología se documentará en /docs/ (fuera de la app).

Qué no hace (deliberadamente)

No muestra direcciones, nombres, descripciones ni categorías de delito.

No permite filtrar por tipos de incidentes.

No “etiqueta” barrios ni señala personas.

No funciona como “alerta en tiempo real” a nivel de calle.

Calidad visual

Mapa base gris + colormap de calor sobrio.

Escala suave y continua; el calor se refina al hacer zoom (capas/tiles vectoriales y agregación por zoom).

Sin elementos estridentes ni leyendas invasivas.

Actualización de datos

Automática (ETL programado) desde las fuentes permitidas.

Regeneración de agregados por periodo y nivel de zoom.

Control de duplicados y señales débiles.

Futuro (planificado, no implementado): un agente de IA que apoye la verificación y actualización de datos navegando fuentes públicas de forma controlada.

Cómo usarlo en local (resumen)

Clona el repo, prepara un archivo de configuración (.env) con las claves del mapa base y los endpoints de datos.

Levanta la UI (frontend) y el servicio de datos (API que sirve las celdas agregadas).

Abre la app en tu navegador.
(Mantendremos guía paso a paso en /docs/instalacion_local.md.)

Contribuciones

Issues bienvenidos (mejor si incluyen contexto, capturas y propuesta concreta).

PRs: prioriza mejoras de usabilidad, privacidad y calidad del mapa.

Nada de añadir detalles que puedan desanonimizar: la simplicidad aquí es una feature, no una carencia.

Roadmap corto

Documentación de fuentes y metodología básica.

Métricas de calidad (cobertura, frescura, estabilidad).

Modo “ligero” para equipos modestos.

Prototipo de agente IA (revisión asistida de fuentes públicas).

Licencia

Creative Commons Attribution–NonCommercial–ShareAlike 4.0 (CC BY-NC-SA 4.0).
Puedes compartir y adaptar con atribución, sin fines comerciales, y manteniendo la misma licencia.
Atribución sugerida: “HitS — Hotspots in Spain (este repositorio)”.

Descargo de responsabilidad

HitS es informativo y preventivo. Puede contener sesgos por cobertura de fuentes, retrasos o geocodificación aproximada. No sustituye a informes oficiales ni a la actuación de autoridades. Use con sentido común.
