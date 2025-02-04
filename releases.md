# JusticIA ecoSystem - La IA de la FEAC

## 2.0.0 (04/02/2025)

:rocket: **NUEVAS FUNCIONALIDADES**

- **Unificación de Assistants dentro de JusticIA Global**:
  - Ahora sólo operamos con un único Assistant, JusticIA Global, al que se le pueden hacer todas las consultas de las diferentes áreas de la FEAC y el OLRC.
  - Ahora este Assistant opera con 6 roles diferentes en función del caso de uso.
  - Se han mejorado mucho las instrucciones para hacerlas más específicas y se ha ajustado la temperatura de respuesta del modelo.
  - Elementos afectados: JusticIA Assistants.

:technologist:	**MEJORAS DE USABILIDAD**

- Se ha modificado el frontend de JusticIA para eliminar el menú de selección de asistentes.
- Se han unificado en este Assistant las 6 funciones especiales.

:books: **ENRIQUECIMIENTO DE BBDD**

- Se han unificado las bases de datos de conocimiento y se han añadido 48 nuevos archivos.
- Estos nuevos archivos incluyen sobre todo jurisprudencia y documentos magisteriales y doctrinales.

## 1.1.0 (24/12/2024)

:rocket: **NUEVAS FUNCIONALIDADES**

- **Nueva función: buscar_google**:
  - Permite introducir un término de búsqueda directamente en el Assistant y que éste busque en Google, examine los primeros 6 resultados, devuelva parte del contenido y lo sintetice con la información más relevante.
  - Elementos afectados: JusticIA Esencial, JusticIA Legal, JusticIA People y JusticIA Copy.
  - *:heart: ¡Gracias JMA!*
- **Nueva función: get_emailing**:
  - Permite recuperar el texto completo de los emailings enviados por la FEAC y por el OLRC para que el Assistant trabaje con ese contexto y producir mejores resultados.
  - Elementos afectados: JusticIA Copy.
  - *:heart: ¡Gracias CRod!*
- **Nuevas funciones: cálculos de probabilidad de donativos y altas de Socio**:
  - Muestra un dictionary detail en SALESmanago con una predicción, elaborada por inteligencia artificial, estimando de 0 a 100:
    - /activationProbability: posibilidad de que un Donante puntual convierta en Socio.
    - /firstPurchaseProbability: posibilidad de que un lead en etapa SQL se convierta en Donante puntual.
    - /addPurchaseProbability: posibilidad de que un Donante puntual vuelva a hacer un donativo puntual.
  - Elementos afectados: JusticIA Copilot (+ automation rules en SALESmanago).

:hammer_and_wrench: **ARREGLOS**

- Arreglo de problemas de autorización en la función para extraer el contenido de una URL (search_and_read_url) en los 4 Assistants.
- Mejora del manejo de errores en el frontend para que aparezca un mensaje con el error y no un mensaje de "código roto".

:technologist:	**MEJORAS DE USABILIDAD**

- Nuevos cuadros de atajos a las funciones de cada Assistant para prerellenar la llamada a la función y reducir errores.

:eyes: **MEJORAS ESTÉTICAS**

- Nuevo mensaje de bienvenida de los Assistants con animación de escritura con cursor.


:books: **ENRIQUECIMIENTO DE BBDD**

- Vector Store JusticIA Esencial: 2 documentos nuevos *(ids #7-#8)*.
- Vector Store JusticIA Legal: 21 documentos nuevos *(ids #85-#105)*.
- Vector Store JusticIA Copy: 3 documentos nuevos *(ids #12, #13, #14)*.

- Code Interpreter JusticIA Legal: 6 documentos nuevos *(ids #2-#7)*.

## 1.0.0 (12/12/2024)

### Funciones generales

- Registro en logs de consola de consultas exitosas y erróneas de todo el ecoSystem.
- Registro en logs de las conversaciones con los Assistants.
- Registro en logs del tiempo de respuesta de cada consulta a los Assistants (y muestra en el frontend).
- Sistema de feedback de la aplicación vía TypeForm.
- Sistema de solicitud de nuevas funcionalidades y reporte de incidencias vía TypeForm.

### JusticIA API

- **/getTicketDescription**: Generar un resumen de cada interacción por email con los usuarios y enviarlo como nota a la ficha del usuario en SALESmanago.
- **/callTranscription**: Generar un resumen de cada interacción por teléfono con los usuarios y enviarlo como nota a la ficha del usuario en SALESmanago.

### JusticIA Assistants

#### JusticIA Esencial

- Chat de inteligencia artificial generativa para aspectos internos generales de la FEAC.
- Navegación por internet para obtener contenido a partir de una URL.

#### JusticIA Legal

- Chat de inteligencia artificial generativa para consultas sobre legislación, producción y revisión de escritos jurídicos, estrategias jurídicas, técnicas de investigación, información sobre nuestros casos, etc.
- Navegación por internet para obtener contenido a partir de una URL.

#### JusticIA People

- Chat de inteligencia artificial generativa para consultas sobre nuestras bases de datos, segmentación, datos sobre usuarios, etc.
- Obtener la lista de notas de un contacto en SALESmanago a partir de un email.
- Navegación por internet para obtener contenido a partir de una URL.
- Obtener el historial de donaciones puntuales de un contacto en SALESmanago a partir de un email.
- Obtener, a partir de un email, una estrategia de telemarketing en base a un conjunto datos del usuario en SALESmanago (información personal, embudo de ventas, etiquetas y peticiones firmadas, standard details, dictionary details, notas del contacto, historial de donaciones puntuales e historial de cuotas de Socio, historial de llamadas de telemarketing).

#### JusticIA Copy

- Chat de inteligencia artificial generativa para consultas sobre copywriting, redacción y supervisión de textos de Marketing, Fundraising y Redes Sociales.
- Navegación por internet para obtener contenido a partir de una URL.

### JusticIA Copilot

- **/purchaseProb**: mostrar en SALESmanago un dictionary detail (copilot_purchaseProbability) con un cálculo de probabilidad de próximo donativo puntual en base a un conjunto de datos del usuario.
