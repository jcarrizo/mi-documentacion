# SOLUCIONES QUE SE FUERON DANDO DURANTE EL PROYECTO EN [NEXTJS]

## module.css

- En Next.js, el archivo page.module.css es un archivo de estilo modular asociado específicamente a una página individual en tu aplicación Next.js.

Cuando creas un archivo nombreDeLaPagina.module.css en el mismo directorio que tu archivo de página (nombreDeLaPagina.js o nombreDeLaPagina.tsx),

los estilos definidos en ese archivo se aplicarán solo a la página con la que están asociados. Esto significa que los estilos definidos en un archivo de módulo CSS

solo afectarán a la página con la que están vinculados y no se filtrarán hacia otras partes de tu aplicación.

==============================================================================

## Toggle del Sidebar

- Al usar el efecto Toggle del Sidebar, se debe agregar en el layout.jsx el script

```javascript
<script
  dangerouslySetInnerHTML={{
    __html: `
                    window.addEventListener("DOMContentLoaded", (event) => {
                      // Toggle the side navigation
                      const sidebarToggle = document.body.querySelector("#sidebarToggle");
                      if (sidebarToggle) {
                        // Uncomment Below to persist sidebar toggle between refreshes
                        // if (localStorage.getItem('sb|sidebar-toggle') === 'true') {
                        //     document.body.classList.toggle('sb-sidenav-toggled');
                        // }
                        sidebarToggle.addEventListener("click", (event) => {
                          event.preventDefault();
                          document.body.classList.toggle("sb-sidenav-toggled");
                          localStorage.setItem(
                            "sb|sidebar-toggle",
                            document.body.classList.contains("sb-sidenav-toggled")
                          );
                        });
                      }
                    });
    `,
  }}
></script>
```

Ademas de respetar la ubicacion de los `<div id="layoutSidenav">` y `<div id="layoutSidenav_content">` , ademas del ID `id="sidebarToggle"`

Dentro de las Pages y el id en el Navbar.

- Para que en sidebar se active el boton de pagina cuando entras en esa , usamos el siguiente comando:

```javascript
className={
                pathname.startsWith("")
                  ? "nav-link  link-body-emphasis"
                  : "nav-link active link-body-emphasis"
}
```

en el caso de este proyecto en el `<a>`, agrego que para el dashboard con link " /" hay que hacer lo siguiente listando los nombres de las paginas

`const listadoPaginas = ["/data-base", "/sell", "/"];` , seguido de :

```javascript
{
  listadoPaginas.map((data) => {
    console.log(data);
    if (pathname == data) {
      return (
        <li key={data}>
          <a
            href="/"
            className={
              pathname == "/"
                ? "nav-link active link-body-emphasis"
                : "nav-link  link-body-emphasis"
            }
          >
            <svg
              xmlns="http://www.w3.org/2000/svg"
              width="16"
              height="16"
              fill="currentColor"
              className="bi bi-house me-3"
              viewBox="0 0 16 16"
            >
              <path d="M8.707 1.5a1 1 0 0 0-1.414 0L.646 8.146a.5.5 0 0 0 .708.708L2 8.207V13.5A1.5 1.5 0 0 0 3.5 15h9a1.5 1.5 0 0 0 1.5-1.5V8.207l.646.647a.5.5 0 0 0 .708-.708L13 5.793V2.5a.5.5 0 0 0-.5-.5h-1a.5.5 0 0 0-.5.5v1.293zM13 7.207V13.5a.5.5 0 0 1-.5.5h-9a.5.5 0 0 1-.5-.5V7.207l5-5z" />
            </svg>
            Inicio
          </a>
        </li>
      );
    }
  });
}
```

==============================================================================

## react-data-table-component

- Al usar react-data-table-component aparece constantemente el error `Error: Hydration failed because the initial UI does not match what was rendered on the server`

Esto lo solucionamos dandole un segundo antes server que cargue la pagina y despues que carge la tabla.

1. add a "loading" state. and some component for showing during this "loading" before rendering the table

2. add useEffect and set this "loading" state to false.

```javascript
// state
const [loader, setLoader] = useState(true);
// effect
useEffect(() => {
  setLoader(false);
}, []);

// render
if (loader) {
  return <div>Loading</div>;
}
return <DataTable pagination columns={columns} data={data} />;
```

==============================================================================

## El código JS se ejecuta dos veces, en el cliente y en el servidor

- Se cambió "reactStrictMode" a "false" en next.config.js y se solucionó. esto hace que los useEffect se ejecuten 2 veces en desarrollo
