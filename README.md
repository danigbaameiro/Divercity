## Divercity
Divercity es una aplicación web para encontrar baños de género neutro.
Las baños de género neutro o unisex pueden proporcionar un espacio más seguro y acogedor para una persona transgénero o que no se identifica con los géneros masculino o femenino, por los cuales los baños públicos a menudo se dividen.

## Motivaciones
La idea de este proyecto surge a raíz de el problema que existe en las ciudades con los baños, ya que estos casi siempre van dirigidos a un género concreto (Masculino/Femenino).

## Licencia
[![License](https://img.shields.io/badge/License-Apache%202.0-blue.svg)](https://opensource.org/licenses/Apache-2.0)
 
## Logo
![alt text](https://github.com/Divercity/Divercity/blob/master/static/img/logo.jpg)

## Frameworks/Tecnologías utilizadas
La aplicación está hecha con Flask(Microframework de Python), HTML5, JavaScript y Bootstrap. La base de datos utilizada es MongoDB.

<b>Hecho con:</b>
- [Flask](http://flask.pocoo.org/)
- [Bootstrap](https://getbootstrap.com/)
- [MongoDB](https://www.mongodb.com)

## Características
La aplicación utiliza la API de Google Maps para representar los baños registrados por los usuarios.

## Estilo del código

[![js-standard-style](https://img.shields.io/badge/code%20style-standard-brightgreen.svg?style=flat)](https://github.com/feross/standard)

## Ejemplo de código
El siguiente código de ejemplo muestra cómo el método principal actúa cuando el usuario inicia la aplicación por primera vez:

```
if request.method == "GET":
        restrooms = []
        restroom = {}
        cursor = mongo.db.collection.find()
        for record in cursor:
            restrooms.append(record)
        return render_template("index.html", restrooms=restrooms, r=restroom)
```
## Instalación
Para su uso en local, se recomienda la utilización de un entorno virtual, como [virtualenv](https://virtualenv.pypa.io), para la instalación de las librerías que se utilizan.
<br>
Para desplegarlo en un servidor, la manera más sencilla es a través de [Heroku](https://www.heroku.com). Aquí tienes una pequeña [cheatsheet](https://github.com/AxelJunes/MLaaS/blob/master/heroku_cheatsheet.txt) para desplegar la aplicación en Heroku.

## Modo de uso
La aplicación cuenta con dos páginas:
- La página principal cuenta con un mapa que contiene marcadores con los baños unisex registrados en la base de datos. Esta página tiene dos botones: "Añadir un baño", que permite añadir un baño nuevo a la aplicación (con un formulario) y "Ver baños cerca de mí", que permite al usuario ver los baños en un radio específico alrededor de él mismo.
- La página de "Sobre Divercity" muestra información sobre la aplicación.

## Créditos
Esta aplicación ha sido desarrollada para la asignatura de Ética, Legislación y Profesión (ELP) perteneciente al cuarto año de los grados en Ingeniera Informática (GII) e Ingeniería del Software (GIW).
