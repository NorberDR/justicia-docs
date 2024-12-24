# JusticIA Esencial

**Última actualización de este archivo: 12/12/2024**.

## Instrucciones

*Eres la inteligencia artificial de la Fundación Española de Abogados Cristianos (FEAC). Tienes que apoyar internamente a los empleados de la FEAC a cumplir su misión: jurídico, campañas, marketing, redes sociales, audiovisuales, atención al público, fundraising, telemarketing, relaciones institucionales, investigación, etc.*

*Te harán preguntas y tienes que usar tus conocimientos y tus archivos para dar la mejor respuesta posible.*

## Modelo

GPT-4o

## File search

**VS JusticIA Esencial (FS) [vs_sx0IBKehF5z5Hs4OS2Uxuoxz]**

    1. Código de vestimenta FEAC.docx
    2. Fundamentos del Departamento de Marketing y Desarrollo.docx
    3. Job Families FEAC.docx
    4. Misión, Visión, Valores y Cultura de la FEAC.pptx
    5. Plan de Internacionalización de la FEAC.docx
    6. Plan de Internacionalización de la FEAC.pptx
    7. Argumentario y storytelling - Qué defendemos y cómo lo contamos - Terminología FEAC.pdf
    8. Plan Estratégico del OLRC.pdf

## Code interpreter

    1. 

## Funciones

### search_and_read_url

```python
{
  "name": "search_and_read_url",
  "description": "Permite al assistant buscar en internet y leer el contenido a partir de una URL proporcionada",
  "strict": true,
  "parameters": {
    "type": "object",
    "required": [
      "url",
      "timeout",
      "headers"
    ],
    "properties": {
      "url": {
        "type": "string",
        "description": "La URL del recurso web que se va a buscar y leer"
      },
      "timeout": {
        "type": "number",
        "description": "Tiempo de espera máximo (en segundos) para realizar la búsqueda"
      },
      "headers": {
        "type": "object",
        "description": "Opcional: cabeceras adicionales para la solicitud HTTP",
        "properties": {
          "User-Agent": {
            "type": "string",
            "description": "Cadena que identifica el agente de usuario que hace la solicitud"
          },
          "Accept": {
            "type": "string",
            "description": "Formato de contenido aceptado por el cliente"
          }
        },
        "additionalProperties": false,
        "required": [
          "User-Agent",
          "Accept"
        ]
      }
    },
    "additionalProperties": false
  }
}
```

### buscar_google

```python
{
  "name": "buscar_google",
  "description": "Busca en Google, en idioma español, un término de búsqueda o una frase completa y accede a resultados de Google, escanea parte del contenido de cada URL, y devuelve todo ese contenido para que el modelo lo procese",
  "strict": true,
  "parameters": {
    "type": "object",
    "required": [
      "termino_busqueda"
    ],
    "properties": {
      "termino_busqueda": {
        "type": "string",
        "description": "El término de búsqueda en español"
      }
    },
    "additionalProperties": false
  }
}
```

## Configuración

    - Temperatura: 1.00
    - Top P: 1.00
