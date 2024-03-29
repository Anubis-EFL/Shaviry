[![en](https://img.shields.io/badge/lang-en-red.svg)](https://github.com/Anubis-EFL/Shaviry/blob/main/README-en.md)
# Shaviry
Adaptador todo en uno del puerto de vídeo de Amiga a VGA con switch de monitores automático y amplificador RGB para minimizar las barras verticales (jail bars) típicas en LCD.

****Advertencia: Esto no es un Scandoubler, tu monitor debe soportar 15khz.****

Sobre el nombre: Shaviry es nuestro agapornis que lleva con nosotros 15 años así que decidí ponerle su nombre para hacerle un homenaje y buscarle un acrónimo, algo forzado pero que mas o menos encaja.
En principio hay dos opciones:

  1) ****SH****arp ****A****miga ****V****ideo ****I****nput switche****R**** s****Y****stem.
  2) ****SH****ort for ****A****miga ****V****ideo ****I****nput switche****R**** s****Y****stem.

Las pruebas han sido en un monitor DELL SE2722HX con una máquina AGA y los amplificadores THS7374 y THS7376.

Con el THS7374 y el filtro activo las barras todavía se perciben un poco y la imagen es un poco borrosa debido a que el ancho de banda del filtro es de solo 9,5mhz.

Con el THS7376 son casi imperceptibles aunque, en ocasiones, las sigo notando si las busco activamente. En uso normal (juegos, demos... etc) la mayoría del tiempo ni las percibo.

No se aprecian en una foto de la pantalla (o casi), por lo que no se si es ya obsesión mía. Por tanto, hasta que pueda hacer mas pruebas, me quedaría con la segunda opción.

De todas formas ahí va la típica foto. Con THS7376 y el filtro activo.

![Image Alt text](/imagenes/Amiga_boot_con_Shaviry.jpg "Boot Screen")

El adaptador tiene unos jumpers para configurar su funcionamiento de dos formas:

 1) Como solo adaptador a VGA por si no dispones de tarjeta gráfica o pistorm (con adaptador de HDMI a VGA)
 2)  Como switch automático de entradas controlado por una señal de 5v.
 
   Esta señal puede ser la que envía switchcontrol por la CIA o el puerto paralelo. En el caso de pistorm puedes sustituir switchcontrol por la opción del driver P96.
  
   Si no quieres usar esas opciónes siempre puedes accionar la conmutación insertando una señal de 5v controlandola con un interruptor, arduino o lo que se te ocurra.

La señal de 5v de conmutación está aislada con un optoacoplador para evitar sustos.

Tambien hay un jumper soldable donde elegir activar o desactivar el filtro del amplificador, hay que elegir una u otra opción, no se debe dejar flotante. Con el THS7376 es recomendable dejarlo activo.

El cambio en un monitor CRT es instantaneo, aunque en un LCD se demora un poco mas.

****Lista de componentes:****
 | Componente | Valor | Tamaño | Cantidad |
 | --- | --- | --- | --- |
 | R1, R2, R3, R4, R5, R6 | 75r | 0603 | 6 |
 | R7 | 1k | 0603 | 1 |
 | R8 | 10k | 0603 | 1 |
 | C1 | 10nf | 0603 | 1 |
 | C2, C3, C4 | 100nf | 0603 | 3 |
 | FB1, FB2, FB3, FB4, FB5 | Ferrita | 0603 | 5 |
 | U1 | 74HCT14 | SO-14 | 1 |
 | U2 | SGM4717 | MSOP-10 | 1 |
 | U3 | THS7373/THS7374/THS7376 | TSSOP-14 | 1 |
 | U4 | SGM330A | SSOP-16 | 1 |
 | U5 | PC817/EL817 | DIP-4 SMD | 1 |
 | J1 | DB23 Hembra | Para cable | 1 |
 | J2, J3 | DB15HD Hembra | Para PCB 3,08mm | 2 |
 | J4 | Tira de 3x2 pines | 2,54mm | 1 |
 | Otros | Jumpers | | 2 |
 
 


Ante todo señalar que soy simplemente un aficionado a la electrónica y es mi primer proyecto en KiCad, así que puede haber cosas mejor hechas.

Mis agradecimientos a Alberto Benitez (Lince / EA4GGE) por sus consejos, sin los cuales probablemente todavía me estaría comiendo la cabeza sobre como enrutar la pcb.
  
## Revisiones:

Las revisiones se nombran como REV seguido de la fecha en formato dd/mm/aaaa

  ****REV19122023****

Revisión inicial. (Publicada el 31/12/2023)

  
 ****REV02012024****

Cambiadas las entradas y salidas del amplificador para que sea totalmente compatible con los THS7373, 7HS7374 Y THS7376.

 ****REV21012024****
 
Cambiado el punto de conexión de la pista de la entrada G del RGB del Amiga al amplificador. No hay cambios en funcionalidad ya que va al mismo sítio pero por otro lado.

 ****REV23012024****

 Eliminadas todas las islas de masa sin conectar.

 
## Agunas imágenes.

Shaviry Con Shaviry
![Image Alt text](/imagenes/Shaviry_adapter_1.jpg "Shaviry con Shaviry")
Shaviry diciendole a Shaviry quien manda.
![Image Alt text](/imagenes/Shaviry_adapter_2.jpg "Shaviry discutiendo con Shaviry")
Algunas Vistas:
![Image Alt text](/imagenes/Shaviry_adapter_3.jpg "Vista 1")
![Image Alt text](/imagenes/Shaviry_adapter_4.jpg "Vista 2")
![Image Alt text](/imagenes/Shaviry_adapter_5.jpg "Vista 3")
![Image Alt text](/imagenes/Shaviry_adapter_6.jpg "Vista 4")
![Image Alt text](/imagenes/Shaviry_adapter_7.jpg "Vista 5")

Junto al adaptador de Commodore. Si, está muy guarro, pero lleva mas de 25 años enchufado a mi Amiga 4000 y ni le he echado cuenta.
![Image Alt text](/imagenes/Shaviry_adapter_8.jpg "Junto al adaptador de Commodore")

## Videos

En un monitor LCD (DELL SE2722HX)


https://github.com/Anubis-EFL/Shaviry/assets/154557850/1416b5dd-fce8-4823-900b-c1d1edef9626

En un monitor CRT (Microvitec 1438) El RTG sale desplazado por no tener totalmente ajustado el modo hdmi de la pistorm32.




https://github.com/Anubis-EFL/Shaviry/assets/154557850/919e8689-20b6-4c1b-af77-966b4a6acc1a

