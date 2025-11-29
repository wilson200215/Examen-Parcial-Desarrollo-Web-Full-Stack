
# Tienda de Repuestos
Elaborado por WILSON MORALES

Descripción:
Aplicación CRUD para gestionar repuestos en una tienda.
Backend: Node.js/Express + MongoDB
Frontend: HTML/CSS/JS (Bootstrap)

Requisitos:
- Node.js (v16+)
- npm
- MongoDB local o Atlas
- Visual Studio Code

Pasos:

1. Configurar variables de entorno
   - Copiar .env.example a .env
   - Editar 
      PORT=4000
      MONGO_URI=mongodb+srv://said_mora:dbHpN4FyvL0rXHsX@cluster0.unfavfw.mongodb.net/test?retryWrites=true&w=majority


     - MongoDB Atlas: mongodb+srv://said_mora:dbHpN4FyvL0rXHsX@cluster0.unfavfw.mongodb.net/

2. Instalar dependencias
   npm install

3. Iniciar backend
   - Con nodemon: npm run dev
   - Sin nodemon: npm start
   - El backend correrá en http://localhost:4000

4. Ejecutar frontend
   - Abrir frontend/index.html con Live Server en VS Code

5. Uso de la API
   Base: /api/parts
   - GET /api/parts → lista repuestos (opcional: search, category, page, limit)
   - GET /api/parts/:id → repuesto por ID
   - POST /api/parts → crear repuesto (JSON body: name, brand, category, vehicleYear, price, stock, sku, description, imageUrl)
   - PUT /api/parts/:id → actualizar repuesto
   - DELETE /api/parts/:id → eliminar repuesto

Notas:
- Asegurarse que MongoDB esté corriendo antes de iniciar backend.
- El frontend utiliza fetch + async/await para manejar repuestos.
- Incluye paginación, filtros por categoría y búsqueda por nombre/SKU.

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
