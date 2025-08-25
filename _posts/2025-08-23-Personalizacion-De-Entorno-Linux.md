---
layout: single
title: Personalizacion De Entorno Linux
date: 2025-08-23
classes: wide
header:
  teaser: /assets/images/slae32.png
categories:
  - Linux
  - Conocimiento General
tags:
  - Linux
  - Conocimiento General
  - 
---


**¿Qué es bspwm? Binary Space Partitioning Window Manager.**

___________________________________________

Es un gestor de ventanas en mosaico (tilling window manager) para x11, esto significa que acomoda las ventanas de forma en que no se superpongan entre ellas. A diferencia de los gestores de ventanas tradicionales como el stacking window managers, donde abres una ventana encima de otra y puedes moverlas libremente, esto no lo permite las ventanas en mosaico.  


Ejemplo de ventana en mosaico:

![Ejemplo de ventana en mosaico:](/assets/images/personalizacion-linux/tillingwindow.png)


Un gestor de ventanas en mosaico tiene estas características: 
- Cada ventana ocupa un espacio definido en la pantalla.
- Cuando abres una nueva ventana, el gestor ajusta automáticamente el tamaño y posición de todas para que quepan sin solaparse.
- Puedes dividir la pantalla en áreas (verticales, horizontales, en cuadrícula, etc.).
- Normalmente se controla mucho con el teclado en lugar del ratón, lo que permite trabajar muy rápido.


Ejemplo de ventana en stacking window:

![Ejemplo de ventana en stacking window:](/assets/images/personalizacion-linux/stackingwindow.png)





**¿Qué es sxhkd? Simple X HotKey Daemon.**

___________________________________________

Es un daemon (proceso en segundo plano) que escucha tus atajos de teclado y ejecuta comandos. El mismo creador de bspwm lo creó para complementarlo, pero puedes usarlo con cualquier otro gestor de ventanas o incluso en escritorios completos.

Ejemplo: 

- Tú dices "Ctrl + Alt + Enter" → sxhkd ejecuta "abre la terminal".
- Tú dices "Super + Q" → sxhkd le dice a bspwm "cierra esta ventana".
- Tú dices "Super + H" → sxhkd le ordena a bspwm "mueve el borde hacia la izquierda".
En otras palabras: sxhkd traduce tus atajos de teclado a comandos.


___________________________________________

¿Por qué los crearon?
Antes de bspwm, otros gestores como i3wm y AwesomeWM mezclaban:

- La lógica de organización de ventanas
- Con los atajos de teclado y configuraciones.


bspwm y sxhkd fueron creados por Bastien Dejean, un programador francés, alrededor de 2013.


-bspwm → Solo administra ventanas (divisiones en mosaico).

-sxhkd → Solo escucha atajos y ejecuta acciones.


**¿Qué es picom?**

___________________________________________

Es un compositor gráfico para las ventanas. Esto significa que se encarga de la transparencia de ventanas, sombras, desenfoque de fondo (blur), transiciones suaves al abrir/cerrar/minimizar.

Sin un compositor, las ventanas se ven planas, sin sombras ni transparencias y se ven muy simples. 



Ejemplo: En Windows 7, cuando activabas Aero Glass y las ventanas se veían transparentes con bordes brillantes, eso era gracias a un compositor. En Linux, ese trabajo lo hace Picom.
Ya que Picom es altamente personalizable y ayuda a que la estetica del escritorio se vea mejor y a tu gusto!   


Ejemplo de windows 7 con Aero Glass:


![Ejemplo de windows 7 con Aero Glass:](/assets/images/personalizacion-linux/aeroglass.png)

En la imagen podemos ver como una ventana de windows tiene diferente nivel de transparencia y se ve mejor esteticamente. Eso hace picom, pero en Linux. 




**¿Qué es la Polybar?**

___________________________________________

La polybar es una barra de estado o tareas altamente personalizable para ventanas X11. Puedes usar la polybar para mostrar informacion como: 

- Hora y fecha
- Uso de CPU, RAM, batería
- Redes, volumen, música
- Workspaces (escritorios virtuales)

Se puede configurar su apariencia y los modulos que muestra. Tiene un estilo minimalista y funcional. 


**¿Qué es Rofi?**

___________________________________________

Rofi es un lanzador de aplicaciones/menu rapido, sirve para que puedes buscar y ejecutar la aplicacion que tu gustes de forma rapida, sencilla y por comandos de teclado. 
Puedes personalizar el rofi con diferentes temas y elegir el que mas te guste, su interfaz es altamente configurable lo que permite configurarla al gusto de uno.

**¿Qué es feh y porque es necesario complementarlo con bspwm?**

___________________________________________

La razon por la que necesitamos feh si vamos a usar bspwm es porque bspwm es un gestor de ventanas, no dibuja fondos ni barras por si mismo. Si queremos añadir un fondo de pantalla con bspwm tenemos que usar un programa externo en este caso usamos feh. 

feh es un programa ligero para Linux que se usa principalmente para mostrar imágenes y poner fondos de pantalla. No consume casi recursos y se ejecuta en segundo plano sin interferir con bspwm. Simple y confiable. 


**¿Qué es la Kitty?**

___________________________________________

Es como tmux solo que con esteroides, en mi parecer es mucho mejor usar la kitty que tmux. La kitty es un emulador de terminal moderno para sistemas operativos basadon en Unix como Linux y macOS. Es conocido por su capacidad de manejar graficos modernos como imagenes y emojis directamente en la terminal.

Es super personalizable e incluye funcionalidades avanzadas como:

- Diferentes pestañas 
- División de ventanas 
- Transparencia 
- En el archivo kitty.config puedes cambiar colores, fuentes, atajos, etc.
