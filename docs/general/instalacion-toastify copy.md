---
sidebar_position: 4
---

# Instalacion Toastify

Libreria de notificaciones toast. **Link: [https://www.npmjs.com/package/react-toastify](https://www.npmjs.com/package/react-toastify).**

- Para usar Toastify se debe agregar en el layout:

```javascript
import { ToastContainer } from "react-toastify";
```

- Ademas de agregar lo siguiente `<ToastContainer />` despues del `{children}`

- Y en la pagina que queres el toast se agrega: `import { toast } from "react-toastify";`
- Ademas de `const notify = () => toast("Wow so easy!");`

- Y en el boton se agrega `onClick={notify}`
