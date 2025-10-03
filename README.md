Principales realizados en base de la plantilla del profesor:

▸ Cambiar productos y crear una nueva API
▸ Incluir Bootstrap (table, button, border y card)
▸ Modificar Css: font-family, color, font-weight, ect


Actividad 1: carrito de la compra agoodshop

Objetivos de la actividad

En esta actividad debes programar la funcionalidad de carrito de la compra de una tienda online ficticia. Aquí pondrás en práctica:
▸	Llamadas a una API.
▸	Manejo y modificación del DOM.
▸	Programación orientada a objetos.

Aunque la tienda es ficticia, la manera de enfocar esta actividad y lo que se requiere no difiere mucho de cómo funciona el mundo real.

Pautas de elaboración

El corazón del carrito de la compra debe ser una clase carrito que es la que se encargue de guardar la información y hacer los cálculos. Te recomiendo que empieces por ahí y, una vez la tengas lista, empieces a maquetar y conectarte a la API. La clase carrito no debe conocer nada acerca del documento HTML ni interactuar con el DOM, simplemente sabe hacer cálculos.

Estos son algunos de los métodos que debe tener la clase carrito (tómalo a modo de guía, puedes añadir otros métodos si lo necesitas):

class Carrito {
    constructor(productos) {
    }

    actualizarUnidades(sku, unidades) {
      // Actualiza el número de unidades que se quieren comprar de un producto
    }

    obtenerInformacionProducto(sku) {
      // Devuelve los datos de un producto además de las unidades seleccionadas
      // Por ejemplo
      // {
      //   "sku": "0K3QOSOV4V",
      //   "quantity": 3
      // } 
    }

    obtenerCarrito() {
      // Devuelve información de los productos añadidos al carrito
      // Además del total calculado de todos los productos
      // Por ejemplo:
      // {
      //   "total": "5820",
      //   "currency: "€",
      //   "products" : [
      //     {
      //       "sku": "0K3QOSOV4V"
      //       ..
      //     }
      //    ]}
      // }
    }
  }


Los productos vendrán de una API. Puedes elaborar tú mismo una gracias a la página https://jsonblob.com/, pegando un JSON, guardándolo y pudiéndolo consultar posteriormente como si fuese una API https://jsonblob.com/api

Este es un JSON que te puede servir para montar tu API:

{
    "currency": "€",
    "products": [
      {
        "SKU": "0K3QOSOV4V",
        "title": "iFhone 13 Pro",
        "price": "938.99"
      },
      {
        "SKU": "TGD5XORY1L",
        "title": "Cargador",
        "price": "49.99"
      },
      {
        "SKU": "IOKW9BQ9F3",
        "title": "Funda de piel",
        "price": "79.99"
      }
    ]
  }

Como verás en la rúbrica, la maqueta en esta actividad no es lo más importante, por lo que no deberías dedicar más tiempo del necesario a ella. Simplemente se requiere que se pueda ver por pantalla algo que permita ver e interactuar con el carrito.

Una vez tengas la maqueta y la clase Carrito, tendrás que escribir código para:
▸	Crear nuevos elementos en el DOM: listado de productos.
▸	Escuchas de ciertos eventos: número de unidades por cada uno de los productos.
▸	Transformaciones del DOM: actualización del apartado TOTAL cada vez que se realiza un cambio.
