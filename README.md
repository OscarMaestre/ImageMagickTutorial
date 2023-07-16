# Tutorial de ImageMagic
## Introducción

ImageMagick es un conjunto de herramientas que se usan desde la línea de comandos y que sirven para hacer operaciones con imágenes. Puede instalarse en Linux usando::

    sudo apt-get install -y imagemagick

Si se usa Windows puede instalarse desde [la web de ImageMagick](https://imagemagick.org/script/download.php)

## La herramienta ``convert``

``convert`` permite convertir imágenes de un formato a otro. Por ejemplo, podemos pasar una imagen de .BMP a .PNG haciendo esto::

    convert imagen.bmp imagen.png

### Haciendo dibujos

En realidad ``convert`` puede hacer muchas cosas más, como por ejemplo dibujar mediante un pequeño lenguaje. Esta operación exige al menos tres cosas:

* Un tamaño de la imagen que se va a generar. Esto se hace con el parámetro ``-size anchoxalto`` .
* Un color de fondo de la imagen. Se usa el parámetro ``xc:<color>``. 
* Un conjunto de operaciones.

Así, por ejemplo podemos construir una imagen llamada ``dibujo1.png`` usando esto::

    convert -size 100x100 xc:white -draw 'line 20,20,60,90' imagenes/dibujo1.png

Y obtenemos esto:

![Imagen generada por convert](imagenes/dibujo1.png)