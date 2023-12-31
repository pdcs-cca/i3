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

# Configuración

El primer paquete a instalar es  [screengrab](https://github.com/lxqt/screengrab) para tomar capturas de pantalla.

![ScreenGrab](images/escritorio.png)

## Cambio a tema obscuro 

El menu de opciones de configuración se muestra presionando las teclas <kbd>Win</kbd> + <kbd>c</kbd>

![aspecto](images/aspecto.png)

## Configuración del touchpad

En el apartado "Mouse & Touchpad" activar ka opción "Tap to click"  toque para click

![aspecto](images/mouse.png)

## Barra de notificaciónes 

La configuración de i3 se lleva a cabo en el archivo $HOME/.config/regolith/Xresources [xresources](https://regolith-desktop.com/docs/howtos/override-xres/)
Una lista de las opciones que pueden ser ajustadas se muestra en la siguiente página: (https://regolith-desktop.com/docs/reference/xresources/)

Para listar los valores actuales utilizar el comando `xrdb -query`, por ejemplo la posición de la barra de notificaciones es inferior "bottom"

~~~bash
$ xrdb -query | grep -i position
i3-wm.bar.position:	bottom
~~~

La siguiente configuración coloc la barra de notificación en la parte superior, el posicionamiento de las ventanas en modo "tabbed", cambio automático al ultimo espacio de trabajo y el foco sigue al puntero del ratón.
~~~xml
i3-wm.bar.position: top
i3-wm.workspace.layout: tabbed 
i3-wm.workspace.auto_back_and_forth: yes
i3-wm.gaps.focus_follows_mouse: yes
~~~

![escritorio2](images/escritorio2.png)

