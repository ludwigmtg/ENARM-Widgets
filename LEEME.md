# Calendario ENARM con frase diaria

## Archivos
- enarm-365.html: código completo del widget.
- frases.md: las 127 frases proporcionadas, sin modificar.
- EBGaramond-VariableFont_wght.ttf: fuente regular del autor.
- EBGaramond-Italic-VariableFont_wght.ttf: fuente italic de la cita.

## Integración en el repositorio existente
1. Descomprime el ZIP en tu computadora.
2. Sustituye el HTML del calendario en la carpeta que ya publica GitHub Pages. Si tu HTML tenía otro nombre, conserva ese nombre para mantener la URL del embed.
3. Sube frases.md y las dos fuentes en ESA MISMA CARPETA, junto al HTML.
4. Guarda los cambios (commit) y espera a que finalice la publicación.
5. Abre la URL publicada. En Notion usa esa misma URL y aumenta un poco la altura del embed; 320–380 px es un punto de partida para escritorio.
6. No subas el ZIP sin descomprimir: GitHub Pages necesita los archivos individuales.

## Rotación diaria
La fecha se calcula en America/Monterrey. La misma frase permanece durante el día, aunque recargues. Cada nuevo día en que abras el widget se elige al azar una frase pendiente. Las 127 frases se muestran antes de reiniciar la lista. Se evita repetir la última frase al comenzar el ciclo siguiente. Los días sin abrir el widget no consumen frases.

El historial se guarda en localStorage, por navegador y por sitio. PC, iPad y iPhone mantienen historiales independientes. Si borras los datos del sitio, el historial comienza de nuevo. Si el navegador bloquea almacenamiento dentro del embed, la selección solo se conserva mientras esa página esté abierta. Para sincronización entre dispositivos se necesitaría almacenamiento compartido adicional.

## Editar frases
Modifica solo frases.md y conserva esta estructura para cada entrada:

> *“Texto de la frase.”*
> — Nombre del autor

No añadas front matter al Markdown. Las frases nuevas se incorporan a las pendientes; las eliminadas se omiten. Cambiar el texto o el autor hace que se considere una entrada nueva. Las entradas idénticas se deduplican.

## Diseño
Frase: EB Garamond italic. Autor: EB Garamond regular. Sin títulos, controles ni fondos adicionales. Tema automático según prefers-color-scheme. La tipografía y la retícula se adaptan al ancho y alto disponibles; los contenedores extremadamente bajos requieren aumentar la altura del embed para permitir una lectura cómoda.

## Fecha del examen
La constante TARGET_DATE del HTML contiene 2027-09-27 como fecha estimada. El último cuadro corresponde a ese día. Se muestran exactamente 365 cuadros.
