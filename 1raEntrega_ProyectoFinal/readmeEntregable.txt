---URLS---

/api/productos

GET: '/' - Listar todos los productos (usuarios y administradores).
GET: '/:id?' - Buscar producto por id (usuarios y administradores).
POST: '/' - Incorporar producto al listado (administradores).
PUT: '/:id' - Actualizar producto por id (administradores).
DELETE: '/:id' - Borra producto por id (administradores).

/api/carrito

POST: '/' - Crea un carrito y devuelve su id (ambos).
DELETE: '/:id' - Vacía un carrito y lo elimina (ambos).
GET: '/:id/productos' - Me permite listar todos los productos guardados en el carrito (ambos).
POST: '/:id/productos' - Para incorporar productos al carrito por su id de producto (ambos).
DELETE: '/:id/productos/:id_prod' - Eliminar un producto del carrito por su id de carrito y de producto (ambos).

Aclaraciones:
 
1) Si se solicita una ruta no permitada al perfil -> { error : -1, descripcion: ruta 'x' método 'y' no autorizada }
2) Ruta no implementada -> { error : -2, descripcion: ruta 'x' método 'y' no implementada}

---DATA---

Productos: id, timestamp, nombre, descripcion, código, foto (url), precio, stock.
Carrito de Compras: id, timestamp(carrito), productos: {id, timestamp(producto), nombre, descripcion, código, foto (url), precio, stock}.

Aclaraciones:

1) Persistir en FileSystem.


