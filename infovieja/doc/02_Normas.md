# NORMAS DE NOMBRAMIENTO Y PAGINACION

## CARPETAS

- Las carpetas privadas se pueden crear anteponiendo a una carpeta un guión bajo: `_folderName`

Esto indica que la carpeta es un detalle de implementación privado y el sistema de enrutamiento no debe considerarla, por lo que la carpeta y todas sus subcarpetas quedan fuera del enrutamiento.

Ejemplo: `app/_components/Navbar/Navbar.jsx`

- Los grupos de rutas se pueden crear envolviendo una carpeta entre paréntesis: `(folderName)`

Esto indica que la carpeta tiene fines organizativos y no debe incluirse en la ruta URL de la ruta.

Ejemplo: `app/(pages)/data-base/page.jsx`

- El nombre de las carpetas internas de Components van en Mayuscula.

Ejemplo: `/_components/Navbar`

- El nombre de las carpetas internas de pages van en minuscula.

Ejemplo: `(pages)/category/pages.jsx`

- El nombre de las carpetas internas de api van en minuscula.

Ejemplo: `api/category/route.js`

==============================================================================

## PAGINAS

- El nombre de las paginas si llevan mas de una palabra, van a ser separados por "-" (guion medio).

Ejemplo: `(pages)/data-base/pages.jsx`

==============================================================================

## ARCHIVOS

- Todos los archivos tipo .js van de tipo .jsx (exceptos los internos de la carpeta API y la que posean funciones).

- El nombre de los archivos css de styles van minuscula.

Ejemplo: `_components/Navbar/navbar.css`

- El nombre de los archivos de Pages van mayuscula.

Ejemplo: `_components/Navbar/Navbar.jsx`

- En el Archivo `.env` se guardaran las variables de entorno y estas deben estar en mayuscula.

Ejemplo: `DATABASE_URL=xxxxxxxxxxxxxx`
