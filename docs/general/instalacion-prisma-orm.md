---
sidebar_position: 3
---

# Instalacion Prisma ORM

Gestor de **Base de Datos** y Creacion de Tablas. **Link: [https://www.prisma.io/](https://www.prisma.io/).**

- Instalar prisma orm con el comando `npm install prisma --save-dev`

- Instalar el cliente " npm install `@prisma/client`

**En este paso elegimos el tipo de base de datos**

- Ejecutar `npx prisma init --datasource-provider sqlite` o `npx prisma init --datasource-provider postgresql` asi definimos que tipo de **Base de Datos** queremos.

- Luego de editar algun campo de la estructura de la base de datos, ejecutar `npx prisma migrate dev --name init` cambiando el init por un nuevo nombre de commit.

- Ejecutar `npx prisma studio` para abrir el gestor de la base de datos y visualizar las tablas.
