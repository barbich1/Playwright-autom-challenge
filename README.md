🚀 Playwright Challenge – SauceDemo Automation

Automated E2E tests using Playwright, TypeScript, and Page Object Model (POM).

Este proyecto automatiza un flujo completo en el sitio:
👉 https://www.saucedemo.com

Incluye login, ordenamiento de productos, selección y agregado al carrito, checkout y verificación final de compra realizada.

🔧 Tecnologías utilizadas

Playwright Test (TypeScript)

Node.js

Page Object Model (POM)

VS Code

📂 Estructura del proyecto
desafio-playwright-saucedemo/
│ package.json
│ tsconfig.json
│ playwright.config.ts
│ README.md
│
├─ pages/
│   login.page.ts
│   inventory.page.ts
│   cart.page.ts
│   checkout.page.ts
│
└─ tests/
    saucedemo.spec.ts

📁 pages/

Contiene los Page Objects, cada uno representando una pantalla de la web:

Page	Función
LoginPage	Login con credenciales válidas
InventoryPage	Validación de inventario, filtros y add to cart
CartPage	Validación del carrito
CheckoutPage	Completar formulario y validar compra final
📁 tests/

Contiene el test E2E que ejecuta el desafío completo.

▶️ Instalación del proyecto

Clonar o descargar el repositorio

Abrir la carpeta en VS Code

Instalar dependencias:

npm install


Instalar navegadores de Playwright:

npx playwright install

▶️ Ejecución de los tests
🔹 Ejecución normal (headless)
npm test

🔹 Ejecutar con navegador visible
npm run test:headed

🔹 Abrir UI de Playwright Test
npm run test:ui

🔹 Abrir reporte HTML de la ejecución
npm run report

🧪 Casos automatizados incluidos
✅ 1) Login con usuario válido

Navegar a https://www.saucedemo.com/

Completar:

Username: standard_user

Password: secret_sauce

Verificar que se accede a la página de productos.

✅ 2) Filtrar productos por precio (Low → High)

En el inventario:

Seleccionar "Price (low to high)"

Validar que el filtro se aplica.

✅ 3) Agregar dos productos al carrito

Agregar los dos primeros productos

Ir al carrito

Validar que haya al menos 2 items agregados.

✅ 4) Checkout y validación de compra

Click en checkout

Completar formulario:

First Name

Last Name

Postal Code

Finalizar la compra

Validar mensaje: “Thank you for your order!”

🏗 Page Object Model utilizado

Cada acción está encapsulada en un objeto de página:

LoginPage → navegación + login

InventoryPage → filtro + agregar productos

CartPage → validación del carrito

CheckoutPage → completar formulario + finalizar compra

Este enfoque mejora:
✔ Mantenibilidad
✔ Escalabilidad
✔ Reutilización de código

✔️ Requerimientos del desafío

Este proyecto cumple completa y exactamente los ejercicios solicitados:

Ejercicio	Estado
Automatizar login	✔️
Filtrar productos por precio	✔️
Agregar 2+ productos al carrito	✔️
Completar checkout	✔️
Validar compra realizada	✔️
🙋‍♀️ Autora

Automatización realizada por Barbara Luana Chacon como parte de un challenge/exámen técnico usando Playwright
