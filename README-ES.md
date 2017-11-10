[![English](http://upload.wikimedia.org/wikipedia/commons/e/e1/Union_Jack_22x16.png "English")](README.md)
[![Italiano](http://upload.wikimedia.org/wikipedia/commons/7/70/Flag_of_italy.png "Italiano")](README-IT.md)
[![Français](http://upload.wikimedia.org/wikipedia/commons/1/14/Flag_of_france.png "Française")](README-FR.md)
[![Deutsch](http://upload.wikimedia.org/wikipedia/commons/4/4b/Flag_of_germany.png "Deutsch")](README-DE.md)
[![Portugues](http://upload.wikimedia.org/wikipedia/commons/a/aa/Flag_of_Portugal_icon.png "Portugues")](README-PT.md)
[![Español](http://upload.wikimedia.org/wikipedia/commons/3/30/Flag_of_spain.png "Español")](README-ES.md)
[![Türkçe](https://upload.wikimedia.org/wikipedia/commons/thumb/b/b4/Flag_of_Turkey.svg/24px-Flag_of_Turkey.svg.png "Türkçe")](README-TR.md)
****
# recalbox-os
**Nuevo : v3.2.11 Corregido el bug de los controladores con el mismo nombre, añadido tema zoid**

**Nuevo : v3.2.4 Nuevo sistema recalbox.conf, nuevo sistema de arranque.**

**Nuevo : v3.2.3 Correcciones de bugs, Joystick analógico y L2/R2 añadidos en la configuración del joystick**

**Nuevo : recalboxOS es ahora compatible con RPi2 !**

**Nuevo : obtén toda la información de recalbox-os en  [WIKI](https://github.com/digitalLumberjack/recalbox-os/wiki)**

El súper repositorio para recalbox.

El propósito de este repositorio es reagrupar los diferentes proyectos de recalbox en uno solo para que luego sea más facil compilar el sistema.

## Presentación
recalboxOS es un sistema ligero incrustado que funciona en la raspberryPi y la raspberryPi 2.

Puedes transformar tu rpi en una plataforma de emulación, soportando hasta 32 sistemas !


## Características 
- Soporta Atari 2600, Atari 7800, NES, Game Boy, Game Boy color, Game Boy Advance, Super Nintendo, Famicom Disk System, Master System, Megadrive (Genesis), Gamegear, Game and Watch, Lynx, NeoGeo, NeoGeo Pocket, FBA (subset), iMame4all (subset), PCEngine, Supergrafx, MSX1/2, PSX, Sega Cd, Sega 32X, Sega SG1000, Playstation, ScummVM, Vectrex, VirtualBoy, Wonderswan.
- Construída con buildroot, por lo que el sistema de archivos root ocupa solo 100MB comprimido.
- Sistema de recuperación basado en NOOBS : reinstala directamente de tu tarjeta sd u obtén la última versión de la red.
- Actualización online.
- Acceso en red a la carpeta rom, capturas de pantalla, guardados.
- Partición rom fat32 : compatible con todos los sistemas.
- La configuración del controlador está en la interfaz : configura una vez, ejecuta todas las veces que quieras.
- Música de fondo en la interfaz.
- PS3 and Shanwan Bluetooth built-in support (plug a controller, unplug and play).
- Francés, Inglés, Portugues (gracias a mgoulart), Español, Alemán y quizá alguna más si participas.
- Interfaz basada en el fantástico EmulationStation2 de Aloshi.
- Optimizada la versión del FBA con soporte de 4 jugadores (yeah Dungeons and Dragons).
- Usados los GPIOs de la RPi como controladores.

## Proyectos
**recalboxOS** es el proyecto principal, que se compone de 3 subproyectos :

- **recalbox-buildroot** : 
https://github.com/digitalLumberjack/recalbox-buildroot (branch recalbox)  
El proyecto recalbox-buildroot es el sistema buildroot. Este crea todo el sistema linux que correrá en recalbox.
Puedes compilar este proyecto, después copia los archivos resultantes en una SD formateada manualmente para hacer funcionar el sistema en la raspberryPi. Pero hay una forma mejor, llamada recalbox-rescue.

- **recalbox-rescue** : 
https://github.com/digitalLumberjack/recalbox-rescue (branch recalbox)  
Basado en el increíble NOOBS del equipo rpi, recalbox-rescue te permite instalar fácilmente retroboxOs y tener una partición de recuperación en tu tarjeta SD. Es un SO mínimo, que descarga retroboxOS, formatea tu tarjeta SD, e instala todo el sistema por ti.
Se comprobará automáticamente si existe alguna nueva versión disponible en la red, antes de instalar la versión en la tarjeta SD.

- **recalbox-emulationstation** : 
https://github.com/digitalLumberjack/recalbox-emulationstation/tree/recalbox-buildroot  
Basado en el increíble emulationstation 2 de Aloshi, la interfaz ha sido modificada ligeramente para tener música ogg de fondo, selección de idioma, soporte de actualizaciones y configuración del controlador.
