# Convenciones editoriales

Esta nota fija las reglas de redacción y composición que rigen `THESIS.md`.
Son restricciones deliberadas, no preferencias de estilo. Cualquier
modificación posterior del artículo debe respetarlas para que el documento
conserve su regularidad. Las herramientas de validación comprueban solo
algunas de ellas; las demás son responsabilidad de quien escribe.

## Idioma

El cuerpo del repositorio está en español de manera intencional. Se trata de
una excepción explícita a las convenciones de documentación y código
únicamente en inglés vigentes en este entorno de trabajo en 2026. La
excepción está justificada por el objeto de estudio, por la lengua de sus
fuentes primarias y por el público lector previsto. Ningún contribuyente ni
agente automatizado debe «corregirla» traduciendo el artículo.

El archivo `README.md` es la única pieza redactada en inglés, por su función
de puerta de entrada. Los nombres de archivo de la carpeta `docs` están en
español por coherencia con su contenido. Los términos técnicos de la
lingüística se emplean en su forma castellana cuando existe y se definen en
su primera aparición. Las abreviaturas de glosa siguen el uso internacional
y no se traducen.

## Tipografía española

Se aplican las normas ortotipográficas del español sin excepción. Las
comillas de primer nivel son las angulares o latinas, "«»", y las inglesas
quedan reservadas al segundo nivel. La raya se usa para los incisos y se
escribe pegada al texto que encierra. No se deja espacio antes de los signos
de dos puntos, punto y coma, ni de cierre de interrogación o exclamación.

Los títulos y encabezados llevan mayúscula únicamente en la primera palabra
y en los nombres propios. Las cursivas, marcadas con asteriscos, se reservan
para las voces en náhuatl, los latinismos y los títulos de obra. Los
morfemas y las formas citadas como formas van en tipografía monoespaciada.
Los siglos se escriben con numeración romana en versalitas allí donde el
medio lo permite, y en romanas simples en Markdown.

## Regla de párrafo

Todo párrafo de prosa del artículo consta exactamente de cuatro oraciones.
La restricción impone un ritmo uniforme y obliga a cerrar cada idea en lugar
de encadenarla indefinidamente. Se exceptúan las listas, las tablas, los
bloques de código y los pies de tabla, que no son prosa corrida. Quien
amplíe el artículo debe mantener la regla o retirarla del documento entero,
nunca aplicarla de manera parcial.

## Citación

Las referencias siguen el estilo APA 7 en su adaptación al español. Las
citas en el texto usan la forma de autor y año entre paréntesis, y la lista
final se ordena alfabéticamente. Se omiten deliberadamente las direcciones
electrónicas, por decisión editorial y porque las obras citadas son
identificables por autor, año y editorial. Las obras primarias reeditadas
indican el año de la edición consultada y, entre paréntesis, el de la
publicación original.

## Personas identificables

El artículo documenta el uso contemporáneo del antropónimo por categorías de
fuente y nunca mediante nombres de personas concretas. La restricción se
aplica aunque los registros de origen sean públicos, porque reunir en un
solo documento datos dispersos sobre individuos privados constituye una
compilación que este trabajo no necesita. La prohibición es absoluta cuando
la persona es o pudo ser menor de edad. Un argumento demográfico correcto se
sostiene con agregados, no con listas nominales.

## Restricciones de formato Markdown

El documento se valida contra la configuración compartida de markdownlint y
no admite configuración local. Las restricciones efectivas son líneas de
ochenta columnas como máximo, incluidas tablas y encabezados; encabezados de
estilo ATX con un único título de primer nivel; viñetas con guion; listas
ordenadas numeradas siempre con «1.»; sangría de dos espacios; ausencia de
HTML incrustado y de direcciones desnudas. Los bloques de código exigen
etiqueta de lenguaje y quedan exentos del límite de columnas. Ningún hallazgo
de la validación se resuelve relajando la configuración compartida.
