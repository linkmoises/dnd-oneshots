# One Shots para Dungeons and Dragons 5e

Muchas veces nos encontramos en el dilema de querer iniciar una partida, pero nuestros jugadores
no tienen la disponibilidad del tiempo para acompañarnos varias sesiones en una campaña. Aquí 
es donde vienen los *one shots*, campañas cortas cuya duración puede ir entre una a cuatro horas.

Creo que una aventura tipo *one shot* bien estructurada puede ser un gran punto de partida 
para introducir jugadores a esto del rol y sobre todo a Dungeons and Dragons 5e. Para acelerar las
cosas, sobre todo con jugadores novatos, sería ideal utilizar los personajes prefabricados de las
cajas de inicio, ya sea la aventura de la Mina de Phandelver o el Dragón de Icespire Pike y hacer 
las modificaciones mínimas necesarias para jugar de manera inmediata.

Algunos de los *one shots* de este repositorio son de mi autoría. Otros son sacados de otros 
sitios web. De algunos, solo está la idea general y termino elaborando los detalles y dándole 
contexto a la aventura. Otros son *one shots* que ya están disponibles pero les vuelvo a dar 
formato usando la plantilla para LaTeX: [dndbook](https://github.com/rpgtex/DND-5e-LaTeX-Template).

Esta plantilla `dndbook` está integrada como submódulo de git en el directorio `lib`. La plantilla
LaTeX en sí mantiene varias dependencias, pero las instalé a medida que obtenía errores de 
compilación, por lo que se me hace dificil enumerarlas de manera específica. Los paquetes que 
instalé en su momento en Arch Linux son: `texlive-fontsrecommended`, `texlive-latexextra`, 
`texlive-langspanish`, `texlive-publishers`, `texlive-plaingeneric`. Es posible que la plantilla 
tenga más dependencias, pero como uso LaTeX rutinariamente, me es un poco difícil saberlo. Para 
utilizarla solo es necesario descargar el submódulo para empezar:

```
cd lib
git submodule init
git submodule update
```

Para compilar los one-shots y obtener ese elegante formato similar al oficial que aparece en los
libros de Dungeons and Dragons, usamos:

```
latexmk -pdf <nombre-de-archivo.tex>
```

Los diseños e ilustraciones son en su mayoría descargados desde internet. Se le da el crédito
a los autores y se enlaza la versión original cuando es posible. Se les da formato con el
editor de imágenes [gimp](https://www.gimp.org/). Los mapas incluidos en las aventuras son 
realizados con la herramienta web [Inkarnate](https://inkarnate.com/).

LaTeX genera muchos archivos intermedios y logs, para limpiar el directorio luego de una o 
varias compilaciones solo es necesario hacer:

```
latexmk -c
```