![header](doc/header.png)

# Trabajo Práctico Final

Autor:

* Jose severiche

Docente:

* Brian Ducca

## Índice de contenidos

1. Introducción 
2. Instalación de dependencias
3. Ejecución de la aplicacion
4. Licencia

## Introducción 

El presente trabajo práctico final de la materia Desarrollo de Aplicaciones Multiplataforma tiene por objetivo el desarrollo de una aplicación que permite controlar un sistema de riego automatizado. Para el desarrollo de esta aplicacion se baso en los conceptos vistos en la materia para implementar una aplicación utilizando como base el framework de Angular para diseñar una página web y mediante el framework Ionic transformarla en una aplicación para dispositivos móviles.

## Instalación de dependencias

Para poder ejecutar el "backend" de la aplicación se debe tener instalado Docker, ya que la aplicación fue desarrollada sobre un contenedor Docker, motivo por el cual es necesario instalar algunas dependencias antes de poder ejecutarla. Antes de realizar los siguientes pasos es necesario tener instalado [Docker](https://docs.docker.com/engine/install/ubuntu/) y [Docker Compose](https://docs.docker.com/compose/install/). En la documentación oficial de Docker y de Docker Compose están los pasos para instalar las herramientas en todas las plataformas.

Para ejecutar la aplicación del "frontend" se requiere tener instalado el framework Ionic. 

Para ello debera tenera en cuenta que:

**Si su computadora cuenta con Node.js instalado**, seguramente cuente con el instalador npm que viene incluído por defecto, por lo que basta con ejecutar el siguiente comando para instalar el framework de Ionic completo:

    $ npm install -g @ionic/cli

Una vez instalado Ionic, esta aplicacion requiere es uso de la biblioteca **Highcharts** para mostrar el gráfico de cada uno de los sensores, debara instalarlo con el siguiente comando:

    $ npm install highcharts --save


**Si ustes no cuenta con Node.js instalado con anterioridad**, en este caso será necesario instalar primero **Node.js** desde la [página de descargas oficial](https://nodejs.org/en/). Una vez finalizada la instalación, se podrán seguir los pasos de la sección anterior para instalar Ionic.



## Ejecución de la aplicación

### Inicialización del "backend"

Una vez que se han instaladas todas las dependencias se podrá ejecutar la aplicación. Para ello, se deberá descargar éste repositorio con el siguiente comando desde una terminal:

        $ git clone https://github.com/severiche90/tp_dam.git

Para inicializar el contenedor, primero se debe acceder desde la terminal al directorio donde se descargó el repositorio ejecutando el siguiente comando:

         cd back

Luego ejecutar el siguiente comando:

         docker-compose up

Una vez iniciado, ya se contará una la API en funcionamiento. Para cerrar el contenedor, se puede correr el comando ``docker-compose down`` desde otra terminal o bien presionar las teclas ``Ctrl+C``, obteniendo el mismo resultado.

NOTA: Puede suceder que la primera vez nodeJS no se pueda conectar a la base de datos, si esto sucede ejecutar

docker-compose down
docker-compose up

### Inicialización del "frontend"

Para mostrar la aplicación a través de una pestaña de un explorador web, se necesita acceder desde una terminal al siguiente directorio

    cd front

una vez que este en directorio front, ejecutar el siguiente comando:

    ionic serve

Con éste último comando, la aplicación comenzará a compilar y en caso de que no existan errores, abrirá una nueva pestaña en la dirección ``http://localhost:8100/home``. Una vez abierta, es posible navegar a través de la misma utilizando la vista web o bien simulando un dispositivo móvil, haciendo ``Ctrl + Shift + I`` para acceder a las herramientas de desarrollador desde un navegador basado en Chromium.

## Licencia

Este proyecto se encuentra publicado bajo la licencia GPLv3. En [este enlace](https://www.gnu.org/licenses/quick-guide-gplv3.html) podrá encontrar más información sobre la misma.

![footer](doc/footer.png)
