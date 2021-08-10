### Desafió 11

##### Changelog

- Implementación de PUB como motor de Plantilla (1-pub)
- Implementación de PUB como motor de Plantilla (2-ejs)
- Agregado .prettierignore para ejs

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

### Formato para PUT / POST

```JSON
{
"title": "Nombre Producto",
"price": 999.99,
"thumbnail": "https://picsum.photos/id/1/200/200"
}
```

### motores de plantillas

- Handlebars
  Para escribir las plantillas es interesante debido a que el HTMl se escribe directamente, aunque hay que aprende la sintaxis y la bloques de codigo son legibles con sus {{}}, el proceso de configuración es un poco mas complejo debido a que hay que tener configurado los path correctamente.
  Es un motor de plantillas agradable de usar
- PUB
  Este motor tiene una configura prácticamente instale y use, su sintaxis es practica pero a veces tener que llevar codigo html o snippets a yml/pug es tedioso a menos que se usen convertidores.
  el codigo resultante dependiendo de como se convierta a veces es complicado de leer sobre todo para el caso de bootstrap que hace uso de muchas clase y el pub esto lo anida con (.) y no logra leer con facilidad.
  Es un motor también entretenido de usar
- EJS
  Este motor tiene una ventaja la cual es usar el mismo codigo JS para hacer la plantilla, pero tiene un inconveniente que puede llegar a frustrar mucho y es dependiendo del editor de texto, el uso de `<%%>` se complica por que no es un tag como del html y tiene en ocasiones a hacer líos como por ejemplo con prettier.
  Es un motor que tiene ventaja pero su sintaxis llega a complicar hacer un debug de que esta fallando.
  Fue rápido cambiar de handlerbars a ejs determinada implementaciones delos otros motores no son aceptadas por que las reglas de JS y tag con tedioso.

De usar un solo motor usaría el de PUB si es un proyecto nuevo, pero si es un proyecto donde se debe llevar html a algún motor de plantilla usaría handlebars.
