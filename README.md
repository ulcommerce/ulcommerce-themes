ulcommerce Themes
=======

Con el fin de que nuestros desarrolladores puedan crear tiendas a medida hemos creado un sencillo sistema de temas de rapida implementación y flexible, el sistema está basado en el sistema de plantillas de PHP <a href="http://twig.sensiolabs.org/" target="_blank">Twig</a>.
 
<a name="id-introduccion"></a>
# I. Archivos y Carpetas

<a name="id-carpetas"></a>
## Carpetas
Hemos tratado de mantener la flexibilidad como principio de nuestros temas aunque se deben mantener una organización en las carpetas con 

La siguiente tabla muestra la estructura general de la API:

> Ejemplo de estructura de un repositorio.

```
/
├── css/
│   ├── bootstrap.css
│   ├── main.css
├── views/
│   ├── index.html
│   ├── base.html
│   ├── blog.html
│   ├── cart.html
│   ├── category.html
│   ├── contact.html
│   ├── product.html
│   ├── make.html
│   ├── page.html 
│   ├── post.html
│   ├── stores.html
├── mails/
│   ├── register.html
│   ├── register.html
└── js/
    ├── bootstrap.js
    └── main.js
```

**NOTA:** Los archivos estaticos deben ser colocados en la raiz .


<a name="id-archivos"></a>
## Archivos
La autenticación al momento de realizar peticiones esta basada en un token propio de cada tienda.

<a name="id-base"></a>
###  - base.html
Este es el archivo que sale en todas las vistas, usualmente tiene el header y footer.

<a name="id-cart"></a>
###  - cart.html
Es la vista del carrito de compras.

<a name="id-index"></a>
###  - index.html
Es la vista del home de la tienda

<a name="id-product"></a>
###  - product.html
Es la vista de los productos de la tienda.

> **NOTA:** "Número" representa el id de la marca que desea listar.

<a name="id-metodos"></a>
# II. Objetos 

<a name="id-marcas"></a>
## Cart

| Objeto | Descripción | 
| ------ | ------ | 
| {{ store.currency }} | Moneda que tiene seleccionada la tienda | 
| {{ cart.total }} | Valor total del carro de compras | 

<a name="id-marcas"></a>
## Pages

| Objeto | Descripción | 
| ------ | ------ | 
| {{ store.currency }} | Moneda que tiene seleccionada la tienda | 
| {{ cart.total }} | Valor total del carro de compras | 

<a name="id-marcas"></a>
## Sections

| Objeto | Descripción | 
| ------ | ------ | 
| {{ store.currency }} | Moneda que tiene seleccionada la tienda | 
| {{ cart.total }} | Valor total del carro de compras | 

<a name="id-marcas"></a>
## Banners

| Objeto | Descripción | 
| ------ | ------ | 
| {{ store.currency }} | Moneda que tiene seleccionada la tienda | 
| {{ cart.total }} | Valor total del carro de compras | 

<a name="id-marcas"></a>
## Categories

| Objeto | Descripción | 
| ------ | ------ | 
| {{ store.currency }} | Moneda que tiene seleccionada la tienda | 
| {{ cart.total }} | Valor total del carro de compras | 


<a name="id-metodos"></a>
# III. Filtros


<a name="id-metodos"></a>
# VI. Variables

<a name="id-metodos"></a>
# VII. Formularios

<a name="id-marcas"></a>
## Login

Para iniciar sesión debe crear un form con <code> method="post" action="/login" </code> y debe tener los siguientes id.

- email
- Passwords

<a name="id-marcas"></a>
## cart

Para agregar un producto al carro debe crear un form con <code>method="post" action="/cart/add"</code> y un input que tenga el valor <code>value="{{ product.idProduct }}"</code>
