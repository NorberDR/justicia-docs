# JusticIA ecoSystem - La IA de la FEAC

JusticIA ecoSystem es la plataforma de inteligencia artificial para uso interno de la Fundación Española de Abogados Cristianos. Tiene como objetivo apoyar al Equipo de la FEAC a realizar mejor su trabajo, agilizar las consultas, apoyar la toma de decisiones y conectar nuestras diferentes herramientas.

Este README está diseñado para ayudar al Equipo a entender qué es JusticIA, de qué se compone, cuáles son sus funcionalidades y la versión actual (y el historial de versiones).

**Versión actual de JusticIA ecoSystem: 2.0.0 (04/22/2025)**.

**Última actualización del README: 04/02/2025**.

## Componentes y funcionalidades de JusticIA

### JusticIA API

Este componente usa el mecanismo de las API para integrarse con otras aplicaciones, recibir y enviar información, y aprovecha la inteligencia artificial para traspasar sólo la información más relevante.

**Funciones**:

   - Generar un resumen de cada interacción por email con los usuarios y enviarlo como nota a la ficha del usuario en SALESmanago.
   - Generar un resumen de cada interacción por teléfono con los usuarios y enviarlo como nota a la ficha del usuario en SALESmanago.

### JusticIA Assistants

Este componente usa la API de OpenAI para mantener conversaciones con un asistente de inteligencia artificial específico para la FEAC: **JusticIA Global**.

**Casos de uso**: uso global para toda la FEAC dentro de 6 posibles roles:

   1. JusticIA Esencial (para brindar información básica sobre la FEAC, su naturaleza, Misión, Visión, Valores, Cultura y políticas para los empleados);
   2. JusticIA Legal (apoyo al Departamento Jurídico con sus estrategias legales, redacción y revisión de documentos legales, etc.);
   3. JusticIA Copy (apoyo a las áreas de Marketing, Expansión Territorial, Fundraising y Redes Sociales y Audiovisuales en la generación de contenido);
   4. JusticIA People (apoyo a las áreas de Fundraising, Telemarketing y Atención al Público en sus consultas sobre el público de la FEAC, segmentos, información sobre los usuarios, etc.);
   5. JusticIA Observatorio (apoyo al área del Observatorio para la Libertad Religiosa y de Conciencia [OLRC] para sus consultas sobre todo el OLRC en todas las áreas),
   6. JusticIA Research (apoyo al Área de Investigación en sus consultas sobre investigación de empresas, personas, instituciones públicas, estrategias de investigación, etc.).

**Funciones extra:**

   - Obtener la lista de notas de un contacto en SALESmanago a partir de un email.
   - Navegación por internet para obtener contenido a partir de una URL.
   - Obtener el historial de donaciones puntuales de un contacto en SALESmanago a partir de un email.
   - Obtener, a partir de un email, una estrategia de telemarketing en base a un conjunto datos del usuario en SALESmanago (información personal, embudo de ventas, etiquetas y peticiones firmadas, standard details, dictionary details, notas del contacto, historial de donaciones puntuales e historial de cuotas de Socio, historial de llamadas de telemarketing).
   - Búsqueda en Google de un término y extraer la información más relevante.
   - A partir de un email enviado por la FEAC, extraer el contenido para añadirlo como contexto a la generación de nuevos contenidos relacionados.

### JusticIA Copilot

Este componente usa la inteligencia artificial para **mostrar sugerencias de actuación en el frontend de otras aplicaciones**:

   - Mostrar en SALESmanago el dictionary detail copilot_firstPurchaseProbability con la probabilidad de que un lead haga su primer donativo.
   - Mostrar en SALESmanago el dictionary detail copilot_addPurchaseProbability con la probabilidad de que un Donante vuelva a hacer un donativo.
   - Mostrar en SALESmanago el dictionary detail copilot_activationProbability con la probabilidad de que un contacto se haga Socio.

## Tecnología

1. **Backend**

   - Lenguaje de programación general: Python
   - Call API de Zendesk (https://developer.zendesk.com/api-reference/sales-crm/resources/calls/)
   - Ticketing API de Zendesk (https://developer.zendesk.com/api-reference/ticketing/introduction/)
   - API de SALESmanago (https://docs.salesmanago.com/)
   - API de OpenAI:
      (a) GPT 4o para JusticIA API, Assistants y Copilot
      (b) Whisper-1 para Justicia API
   - S3 de Amazon Web Services (AWS)
   - API de Gmail (https://developers.google.com/gmail/api/reference/rest?hl=es-419)
   - Google Search API SERPAPI (https://serpapi.com/search-api)

2. **Frontend**

   - HTML
   - CSS
   - JavaScript
   - TypeForm

## Funcionalidades de uso

   - Registro en logs de consola de consultas exitosas y erróneas de todo el ecoSystem
   - Registro en logs de las conversaciones con los Assistants
   - Registro en logs del tiempo de respuesta de cada consulta a los Assistants (y muestra en el frontend)

## Comentarios

Para cualquier comentario, sugerencia o incidencia con JusticIA, contactar con **ndominguez@abogadoscristianos.net**.
