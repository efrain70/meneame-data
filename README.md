# MeneaData 
[![Build Status](https://travis-ci.org/efrain70/meneadata.svg?branch=ci)](https://travis-ci.org/efrain70/meneadata)
[![Coverage Status](https://coveralls.io/repos/github/efrain70/meneadata/badge.svg?branch=master)](https://coveralls.io/github/efrain70/meneadata?branch=master)

## Índice

1. [Introducción](#introduction)
    1. [Menéame](#meneame)
    2. [El valor de los datos](#value)
    3. [MeneaData](#meneadata)
2. [Instalación](#installation)
3. [Cómo usarlo](#usage)
    1. [Ejemplos](#examples)
    2. [Dataset](#dataset)
4. [Colaborar](#contributing)
5. [Autoría](#authors)
6. [TODO](#todo)  

## Introducción <a name="introduction"></a>

Este proyecto nace por la necesidad de poder obtener los datos
publicados en el sitio web <a href="https://www.meneame.net/" target="_blank"> Menéame</a>.

### Qué es menéame <a name="meneame"></a>
Menéame es un sitio web donde los usuarios registrados envían noticias (meneos) que pueden ser votadas
por los demás usuarios. Las noticias más votadas (con más meneos) se publican 
en la página principal usando cómo criterios no sólo el número de votos sino otros aspectos como
el "karma" o el número de votos negativos. Los usuarios registrados forman a su vez una red social
que interactúa a través del sistema de votaciones y los comentarios con el resto de usuarios.
​
 
### El valor de los datos en Menéame <a name="value"></a>

Actualmente se encuentra entre los 150 sitios webs más visitados en España y en los 5000 del mundo según
el ranking Alexa (https://www.alexa.com/siteinfo/meneame.net). Con 11.3 millones de visitas al mes y más de
70000 noticias llevadas a portada es uno de los sitios más relevantes en España.

### MeneaData <a name="meneadata"></a>

La principal intención de este proyecto es la extracción de información contenida en este sitio web
para estudios basados en los datos publicados de los envíos de noticias (meneos) y de su red social.

El portal cuenta actualmente con una API bastante limitada que no permite la lectura automática
de los datos publicados en el sitio. 


## Instalación <a name="installation"></a>

El código fuente está publicado bajo licencia GNU Affero General (versión 3) en 
<a href="https://github.com/efrain70/meneadata" target="_blank"> GitHub</a>.

Para instalarlo sólo es necesario clonar el repositorio:

`$ git clone https://github.com/efrain70/meneadata.git`

Y usando <a href="https://pip.pypa.io/en/stable/" target="_blank"> PIP</a>, configurarlo localmente:

`$ pip install -e meneadata`

## Cómo usarlo <a name="usage"></a>

Después de la instalación se dispone de un comando 'meneadata' con el siguiente formato:

`meneadata -f path_fichero.csv [-v] [-s primera página] [-l última pagina] [-log fichero de log] [-v nivel output]` 

### Ejemplos <a name="examples"></a>

* Simple, imprime la salida en el fichero c://users/User/MyData.csv

`meneadata -f c://users/User/MyData.csv`

* Extrae los datos desde la página 3 a la 1000

`meneadata -f c://users/User/MyData.csv -s 3 -l 1000`

* Cambia el nivel de los mensajes de logging  y los guarda en un fichero local.

`meneadata -f c://users/User/MyData.csv -v -log c://users/User/MyLog.log`

### Estructura Dataset <a name="dataset"></a>

El fichero CSV (Comma=Separated Values) obtenido se compone de los siguientes atributos (columnas):

* votes: número de meneos
* title: título del meneo
* author: autor del meneo
* n_comments: número de comentarios
* karma: karma del meneo
* timestamp: timestamp de la publicación del meneo


## Colaborar  <a name="contributing"></a>

Este proyecto está abierto a mejoras, cambios, propuestas y aportaciones. ¡Colabora!

## Autoría  <a name="authors"></a> 

Desarrolladores:

* Efraín Lima Miranda <efrain70@gmail.com>


## Siguientes pasos <a name="TODO"></a>

* Añadir nuevos campos de los meneos
* Añadir opciones para el comando 
* Introducir los comentarios de cada meneo en el dataset
* Poder exportar en varios formatos
* Selección de los atributos a exportar

