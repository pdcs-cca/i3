# i3

i3 es un gestor de ventanas en mosaico diseñado para X11, inspirado en wmii, y escrito en lenguaje C.
Como wmii, i3 utiliza un sistema de control muy similar a vi. Por defecto, la selección de ventana activa es 
controlada por el 'Mod1' (Tecla Alt/Tecla Super) y las teclas de la fila central de la mano derecha (Mod1+J,K,L,;), 
mientras el movimiento de las ventanas es manejado añadiendo la tecla Tecla Shift (Mod1+Shift+J,K,L). 
[Ggestor de ventanas i3](https://es.wikipedia.org/wiki/I3_(gestor_de_ventanas))


En informática, un Gestor de Ventanas en Mosaico (Tiling Window Manager, en inglés), es un administrador de ventanas 
con una organización de la pantalla en marcos que no se superponen entre sí, a diferencia del enfoque más popular de 
apilamiento basado en coordenadas de objetos superpuestos (ventanas) que intenta emular completamente la metáfora de escritorio. 
[Gestor de ventanas en mosaico](https://es.wikipedia.org/wiki/Gestor_de_ventanas_en_mosaico)

# Regolith

Regolith es un entorno de escritorio moderno construido sobre Ubuntu, GNOME e i3, diseñado para permitirle trabajar más rápido al reducir el desorden y la 
ceremonia innecesarios. 

La mejor forma de probar el manegador de ventanas i3 es descargando la versión "live" de [Regolith](https://regolith-desktop.com/): 

~~~bash 
curl -LO# https://github.com/regolith-linux/regolith-ubuntu-iso-builder/releases/download/ubuntu-kinetic-2.2.0-20221211_050200/regolith-ubuntu-kinetic-2.2.0.zip
~~~

Después de descomprimir se puede utilizar el comando  `dd` para escribir el archivo ISO en una memoria USB. 

** Se asume /dev/sdb  como el dispositivo USB, puede ser diferente en otros equipos **
~~~bash
dd if=ubuntu-22.04.2-desktop-amd64.iso of=/dev/sdb status=progress oflag=direct bs=2M
~~~

## Configuración

