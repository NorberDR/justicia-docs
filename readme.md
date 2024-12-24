# JusticIA ecoSystem - La IA de la FEAC

JusticIA ecoSystem es la plataforma de inteligencia artificial para uso interno de la Fundación Española de Abogados Cristianos. Tiene como objetivo apoyar al Equipo de la FEAC a realizar mejor su trabajo, agilizar las consultas, apoyar la toma de decisiones y conectar nuestras diferentes herramientas.

Este README está diseñado para ayudar al Equipo a entender qué es JusticIA, de qué se compone, cuáles son sus funcionalidades y la versión actual (y el historial de versiones).

**Versión actual de JusticIA ecoSystem: 1.1.0 (24/12/2024)**.

**Última actualización del README: 24/12/2024**.

## Componentes y funcionalidades de JusticIA

### JusticIA API

Este componente usa el mecanismo de las API para integrarse con otras aplicaciones, recibir y enviar información, y aprovecha la inteligencia artificial para traspasar sólo la información más relevante.

**Funciones**:

   - Generar un resumen de cada interacción por email con los usuarios y enviarlo como nota a la ficha del usuario en SALESmanago.
   - Generar un resumen de cada interacción por teléfono con los usuarios y enviarlo como nota a la ficha del usuario en SALESmanago.

### JusticIA Assistants

Este componente usa la API de OpenAI para mantener conversaciones con asistentes de inteligencia artificial específicos para varias áreas de la FEAC.

Actualmente disponemos de estos 4 asistentes:

   **(1) JusticIA Esencial**

**Información general sobre la FEAC** (políticas, guías, documentos estratégicos, etc.).

**Funciones extra:**

   - Navegación por internet para obtener contenido a partir de una URL.
   - Búsqueda en Google de un término y extraer la información más relevante.

   **(2) JusticIA Legal**

Uso de la inteligencia artificial generativa para **consultas sobre legislación, producción y revisión de escritos jurídicos**, estrategias jurídicas, técnicas de investigación, información sobre nuestros casos, etc.

**Funciones extra:**

   - Navegación por internet para obtener contenido a partir de una URL.
   - Búsqueda en Google de un término y extraer la información más relevante.

   **(3) JusticIA People**

Uso de la inteligencia artificial generativa para **consultas sobre nuestras bases de datos, segmentación, datos sobre usuarios, etc.** También dispone de funciones que permiten manejar los datos de los usuarios para usarlos para fines de Telemarketing, Fundraising y Marketing.

**Funciones extra:**

   - Obtener la lista de notas de un contacto en SALESmanago a partir de un email.
   - Navegación por internet para obtener contenido a partir de una URL.
   - Obtener el historial de donaciones puntuales de un contacto en SALESmanago a partir de un email.
   - Obtener, a partir de un email, una estrategia de telemarketing en base a un conjunto datos del usuario en SALESmanago (información personal, embudo de ventas, etiquetas y peticiones firmadas, standard details, dictionary details, notas del contacto, historial de donaciones puntuales e historial de cuotas de Socio, historial de llamadas de telemarketing).
   - Búsqueda en Google de un término y extraer la información más relevante.

   **(4) JusticIA Copy**

Uso de la inteligencia artificial generativa para **consultas sobre copywriting, redacción y supervisión de textos de Marketing, Fundraising y Redes Sociales**.

El Assistant está configurado para proporcionar copies según una serie de buenas prácticas y reglas de formato de la FEAC para:

   - Peticiones de firmas
   - Emailings de fundraising
   - Cartas de fundraising postal
   - Copy para RRSS según el medio

**Funciones extra:**

   - Navegación por internet para obtener contenido a partir de una URL.
   - Búsqueda en Google de un término y extraer la información más relevante.


### JusticIA Copilot

Este componente usa la inteligencia artificial para **mostrar sugerencias de actuación en el frontend de otras aplicaciones**:

   - Mostrar en SALESmanago un dictionary detail (copilot_purchaseProbability) con un cálculo de probabilidad de próximo donativo puntual en base a un conjunto de datos del usuario.

## Tecnología

1. **Backend**

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
