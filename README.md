# DGGSM datamaps
Repositorio compuesto de todos los datasets de la DGGSM, mapeados y agrupados por GO y Proyecto. 
Este repo funciona como un hoster para los html que luego se insertan en iframes en las web que correspondan. 

### Para crear el HTML

Se debe reemplazar el script de generación de la visualización base, luego de que Kepler haga la generación del archivo con toda la configuración definida. 
El elemnto a ser reemplazado es el siguiente script: 

Y debe ser reemplazado por la ultima versión confirmada como funcional:

------------------------

### Para crear el iFrame


```html
<iframe src="https://kepler.gl/#/demo?mapUrl=https://drive.google.com/file/d/1ZDJQpvlF5eYFjMEuxPWIT0e4xkMDNyTW/view?usp=sharing" style="border:0px #ffffff none;" name="myiFrame" scrolling="no" frameborder="1" marginheight="0px" marginwidth="0px" height="500px" width="1200px" allowfullscreen></iframe>
```

Primero se llama a Kepler, que luego abre una JSON o HTML en la segundo parte de la URL.
El HTML debe estar hosteando en un lugar donde se pueda acceder a un Raw, sin que exista verificación de permisos.

---------------------------

### Para crear el iFrame filtrable

En el caso de que quiera que el iframe tenga el recuadro de datasets y filtros, puedo simplemente utilizar la generación base: 

```html 
<iframe src="https://kepler.gl/#/demo?mapUrl=https://raw.githubusercontent.com/ikespand/ikespand.github.io/master/_data/sample_data/keplergl_road_network.json" style="border:0px #ffffff none;" name="myiFrame" scrolling="no" frameborder="1" marginheight="0px" marginwidth="0px" height="800px" width="600px" allowfullscreen></iframe>
```

El segundo link insertado corresponde a un JSON exportado con toda la info de los datasets y la configuración ya definida. Se puede generar en [[Kepler.gl]] desde Share/Export Map/JSON y luego hostear en [[Github de Tade]] sacando el user content del Raw. 

