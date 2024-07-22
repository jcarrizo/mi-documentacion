---
sidebar_position: 2
---

# Instalacion Boostrap

Componentes y Stiling para el proyecto. **Link: [https://getbootstrap.com/docs/5.3/getting-started/introduction/](https://getbootstrap.com/docs/5.3/getting-started/introduction/).**

- Instalar Boostrap con el comando `npm i bootstrap@5.3.3` o la version que este para ese momento.

- Despues se agrega los script al final del Body

```javascript title="index.js"
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

- Ademas de agregar en el mismo index.

```javascript title="index.js"
import "bootstrap/dist/css/bootstrap.min.css
```

o en vez de instalar usar lo siguiente en el Head y eso reemplaza la instalacion:

```javascript title="index.js"
  <link href="https://cdn.jsdelivr.net/npm/bootstrap@5.3.3/dist/css/bootstrap.min.css" rel="stylesheet" integrity="sha384-QWTKZyjpPEjISv5WaRU9OFeRpok6YctnYmDr5pNlyT2bRjXh0JMhjY6hW+ALEwIH" crossorigin="anonymous">
```
