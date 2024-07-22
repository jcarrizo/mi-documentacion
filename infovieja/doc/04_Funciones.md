# FUNCIONES Y USOS DE [NEXTJS]

## {CHILDERN}

- En Next.js 13, al igual que en versiones anteriores, puedes utilizar la prop `{children}` para renderizar

contenido dentro de componentes de React. La prop children es especial porque te permite pasar elementos hijos

a un componente y luego manipularlos o renderizarlos dentro del componente padre.

Ejemplo:

- Puedes usar la prop children para pasar cualquier contenido adicional que desees renderizar dentro del cuerpo del Card.

```javascript
// Card.js
import React from "react";

const Card = ({ title, children }) => {
  return (
    <div className="card">
      <h2>{title}</h2>
      <div className="card-body">{children}</div>
    </div>
  );
};

export default Card;
```

- Luego, en otro componente, puedes usar el componente Card y pasar el contenido que desees dentro de él usando la prop `children`:

```javascript
// OtroComponente.js
import React from "react";
import Card from "./Card";

const OtroComponente = () => {
  return (
    <div>
      <Card title="Mi tarjeta">
        <p>Contenido dentro de la tarjeta.</p>
        <button>Botón dentro de la tarjeta</button>
      </Card>
    </div>
  );
};

export default OtroComponente;
```

En este ejemplo, el componente OtroComponente utiliza el componente Card y pasa un párrafo y un botón como hijos.

Estos elementos se renderizarán dentro del componente Card donde se encuentre `{children}`.

==============================================================================
