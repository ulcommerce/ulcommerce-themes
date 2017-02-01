ulcommerce Themes
=======

Con el fin de que nuestros desarrolladores puedan crear tiendas a medida hemos creado un sencillo sistema de temas de rapida implementación y flexible, el sistema está basado en el sistema de plantillas de PHP <a href="http://twig.sensiolabs.org/" target="_blank">Twig</a>.
 
<a name="id-introduccion"></a>
# I. Archivos y Carpetas

<a name="id-carpetas"></a>
## 1. Carpetas
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
## 2. Archivos
La autenticación al momento de realizar peticiones esta basada en un token propio de cada tienda.

<a name="id-lisMar"></a>
###  - base.html
Ejemplo para listar marcas de productos, url de prueba:
http://ulcommerce/api/v0.1/ulc_plus/01542e2b2bd0bba14/list-make

Para listar todas las marcas simplemente se realiza la petición a la url anterior ( Sin pasar ningún parametro ), si se desea una marca específica se debe enviar el siguiente JSON:

> **NOTA:** "Número" representa el id de la marca que desea listar.

<a name="id-metodos"></a>
# II. Objetos 

<a name="id-marcas"></a>
## Cart

| Objeto | Descripción | 
| ------ | ------ | 
| {{ store.currency }} | Moneda que tiene seleccionada la tienda | 
| {{ cart.total | price }} | Valor total del carro de compras | 
