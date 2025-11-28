Tienda de Repuestos

-Descripción
Aplicación CRUD para gestionar repuestos (Node.js + Express + MongoDB + frontend HTML/JS/CSS). Las imágenes se almacenan como URL en el documento.

-Estructura
- backend/
  - config/db.js
  - controllers/partsController.js
  - models/Repuesto.js
  - routes/parts.js
  - server.js
- frontend/
  - index.html
  - script.js
  - styles.css

-Requisitos
- Node.js >= 14
- MongoDB Atlas (URI en .env)
- npm install

-Ejecución (backend)
1. Copiar `.env` en `backend/` con:
PORT=4000
MONGO_URI=mongodb+srv://said_mora:dbHpN4FyvL0rXHsX@cluster0.unfavfw.mongodb.net/test?retryWrites=true&w=majority

--Frontend

Abrir frontend/index.html en el navegador (o servir con Live Server).

--Rutas de la API

GET /api/parts : listar repuestos (query params: page, limit, search, category)

GET /api/parts/:id : obtener repuesto por id

POST /api/parts : crear (body JSON): name, brand, sku, category, vehicleYear, price, stock, description, imageUrl

PUT /api/parts/:id : actualizar (body JSON, mismos campos)

DELETE /api/parts/:id : eliminar
