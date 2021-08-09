### Desafió 11

##### Changelog

- Implementación de PUB como motor de Plantilla (01-pub)

### Rutas

- GET /api/producto/listar
  Lista los productos disponibles en formato JSON
- GET /api/producto/listar/id
  Lista un unico producto si este existe
- DELETE /api/productos/borrar/id
  Eliminar el producto si existe el id
- POST /api/guardar
  Permite guarda un elemento nuevo.
- PUT /api//productos/actualizar/id
  Permite modificar un elemento si este existe

### Formato para PUT POST

{
"title": "Nombre Producto",
"price": 999.99,
"thumbnail": "https://picsum.photos/id/1/200/200"
}
