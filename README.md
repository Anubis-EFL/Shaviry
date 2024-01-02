# Shaviry
Adaptador todo en uno del puerto de vídeo de Amiga a VGA con switch de monitores automático y amplificador RGB para intentar minimizar las barras verticales (jail bars).

****Advertencia: Esto no es un Scandoubler, tu monitor debe soportar 15khz.****

Sobre el nombre: Shaviry es nuestro agapornis que lleva con nosotros 15 años así que decidí ponerle su nombre para hacerle un homenaje y buscarle un acrónimo, algo forzado pero que mas o menos encaja.
En principio hay dos opciones:

  1) SHarp Amiga Video Input switcheR sYstem.
  2) SHort for Amiga Video Input switcheR sYstem.

Aunque solo he podido probarlo por el momento en un solo monitor (DELL SE2722H) de momento las barras todavía se perciben un poco aunque algo menos que en el adaptador de Commodore,
por lo menos en ese monitor concreto. Por lo tanto, hasta que pueda solucionar eso,  me quedaría con la segunda opción.

El adaptador tiene unos jumpers para configurar su funcionamiento como solo adaptador de VGA por si no dispones de tarjeta gráfica o pistorm (con adaptador de HDMI a VGA)
o como switch automático de entradas controlado por switchcontrol o, en el caso de pistorm, con la opción del driver P96. Si no quieres usar esa opción siempre puedes 
accionar la conmutación insertando una señal de 5v, ya sea con un interruptor, arduino o lo que se te ocurra. La señal de 5v de conmutación está aislada con un optoacoplador para evitar sustos.

El cambio en un monitor CRT es instantaneo, aunque en un LCD, por lo menos en el que he probado, se demora un poco mas.

Tambien hay un jumper soldable donde elegir activar o desactivar el filtro del amplificador, hay que elegir una u otra, aunque el filtro emborrona un poco la imagen del Amiga con el THS7374, falta probar el THS7376.

****Lista de componentes:****
 | Componente | Valor | Tamaño |
 | --- | --- | --- |
 | R1, R2, R3, R4, R5, R6 | 75r | 0603 |
 | R7 | 1k | 0603 |
 | R8 | 10k | 0603 |
 | C1 | 10nf | 0603 |
 | C2, C3, C4 | 100nf | 0603 |
 | FB1, FB2, FB3, FB4, FB5 | Ferrita | 0603 |
 | U1 | 74HCT14 | SO-14 |
 | U2 | SGM4717 | MSOP-10 |
 | U3 | THS7373/THS7374/THS7376 (por determinar el mejor) | TSSOP-14 |
 | U4 | SGM330A | SSOP-16 |
 | U5 | PC817/EL817 | DIP-4 SMD |
 | J1 | DB23 Hembra | Para soldar en cable |
 | J2, J3 | DB15HD Hembra | Soldar en placa (tamaño próximamente) |
 | J4 | Tira de 3x2 pines para jumper | 2x3 2,54mm |
 | Extras | 2 jumpers | |
 
 


Ante todo señalar que soy simplemente un aficionado a la electrónica y es mi primer proyecto en KiCad, así que puede haber cosas mejor hechas.

Mis agradecimientos a Alberto Benitez (Lince / EA4GGE) por sus consejos, sin los cuales probablemente todavía me estaría comiendo la cabeza sobre como enrutar la pcb.
  
## Revisiones:

  ****REV19122023****

Revisión inicial.

  
 ****REV02012024****

Cambiadas las entradas y salidas del amplificador para que sea totalmente compatible con los THS7373, 7HS7374 Y THS7376.

   
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


English

All in one Amiga video port adapter to VGA with auto monitor switcher and RGB amplifier.

Coming soon...
