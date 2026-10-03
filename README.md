# Admin de Productos

Página web de administración de productos (HTML, CSS y JavaScript) con pruebas end-to-end en **Cypress** e integración continua con **GitHub Actions**.

## Funcionalidades

- Inicio de sesión de demostración (usuario `admin`, contraseña `1234`).
- Catálogo de productos cargado desde `public/productos.csv` y guardado en `localStorage`.
- Agregar, editar y eliminar productos, con validación (no se permite precio 0).
- Los productos sin stock se muestran como **Agotado**.

## Estructura

```
public/            Página (index.html, app.js, estilos.css, productos.csv)
cypress/e2e/       Pruebas Cypress (admin.cy.js)
.github/workflows/ Workflow que corre las pruebas en cada push y pull request
```

## Cómo ejecutarlo

```bash
npm install
npm start            # sirve la página en http://localhost:3000
npm run cypress:open # abre Cypress en modo interactivo
npm run cypress:run  # corre las pruebas en consola
```

## Pruebas

1. Login correcto muestra el panel
2. Login incorrecto muestra error
3. Agregar un producto lo añade a la tabla
4. Validación: no deja agregar con precio 0
5. Eliminar un producto lo quita de la tabla
6. Editar un producto actualiza su nombre
7. Un producto agotado se muestra como Agotado
