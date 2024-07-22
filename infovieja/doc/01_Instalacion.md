# Creacion de Proyecto en [NEXTJS]

Sistema Back - Front basado en React. URL: [https://nextjs.org/docs/getting-started/installation]

- Primer Comando `npx create-next-app NombreProyecto`

TypeScript? ... No
ESLint? ... Yes
Tailwind CSS? ... No
src/ directory ... yes
App Router? (recommended) ... Yes
import alias? ... No

- Abrir Terminal dentro del proyecto y ejecutar `npm run build`, asi se genera el proyecto

- Ejecutar `npm run start`, asi se levanta el proyecto

- Para ver el localHost en el telefono u otro dispositivo, se debe abrir el cmd e ingresar `ipconfig`,

buscar tu `Dirección IPv4. . . . . . . . . . . . . . : xxx.xxx.x.xxx`

y en el buscador de tu telefono colocar `xxx.xxx.x.xxx:tu nummero de puerto` , en mi caso 3000

Obviamente debe estar ejecuando el localHost con el proyecto levantado.

==============================================================================

## BOOSTRAP

Componentes y Stiling para el proyecto. URL: [https://getbootstrap.com/docs/5.3/getting-started/introduction/]

- Instalar Boostrap es con el comando `npm install bootstrap` y agregando los script en el Body del layout

```javascript
<script
          src="https://cdn.jsdelivr.net/npm/@popperjs/core@2.11.8/dist/umd/popper.min.js"
          integrity="sha384-I7E8VVD/ismYTF4hNIPjVp/Zjvgyol6VFvRkX/vR+Vc4jQkC+hVqc2pM8ODewa9r"
          crossOrigin="anonymous"
        ></script>
<script
          src="https://cdn.jsdelivr.net/npm/bootstrap@5.3.3/dist/js/bootstrap.min.js"
          integrity="sha384-0pUGZvbkm6XF6gxjEnlmuGrJXVbNuzT9qBBavbLwCsOGabYfZo0T0to5eqruptLy"
          crossOrigin="anonymous"
        ></script>
```

Ademas de agregar el CSS: `import "bootstrap/dist/css/bootstrap.min.css"`

==============================================================================

## PRISMA ORM DB

Gestor de Base de Datos y creacion de Tablas. URL:[https://www.prisma.io/]

- Instalar prisma orm `npm install prisma --save-dev`

- Instalar " npm install `@prisma/client`

  **En este paso elegimos el tipo de base de datos**

-Ejecutar `npx prisma init --datasource-provider sqlite` o `npx prisma init --datasource-provider postgresql`

Luego de editar algun campo de la estructura de la base de datos ejecutar `npx prisma migrate dev --name init` cambiando el init por un nuevo nombre

- Ejecutar `npx prisma studio` para abrir el gestor de la base de datos

==============================================================================

## TOASTIFY

Libreria de notificaciones toast. URL: [https://www.npmjs.com/package/react-toastify]

- Para usar Toastify se debe agregar en el layout: `import { ToastContainer } from "react-toastify"; `

ademas de <ToastContainer /> despues del {children}

y en la pagina que queres el toast se agrega: `import { toast } from "react-toastify";`

ademas de `const notify = () => toast("Wow so easy!");`

y en el boton se agrega `onClick={notify}`

==============================================================================

## REACT DATA TABLE COMPONENT

Tabla para la visualizacion de datos en el programa. URL: [https://react-data-table-component.netlify.app/?path=/docs/getting-started-intro--docs]

- Instalar RDTC con el comando: `npm install react-data-table-component styled-components`

- Donde se visualice la tabla , debe llevar el comando `import DataTable from 'react-data-table-component'`

- Seguido del componente

```javascript
<DataTable columns={columns} data={data} />
```

==============================================================================
