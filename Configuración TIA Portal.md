# Configuración de TIA Portal

Antes de comenzar a trabajar con TIA Portal es recomendable tener una pequeña base de conocimientos sobre como funciona el programa. Para ello adjuntamos algunos enlaces a videos que pueden ser utiles para empezar en el programa. 

Inicio en TIA Portal: Crear proyecto, agregar dispositivo, configurar IP del dispositivo (recomendado hasta minuto 40 como mínimo)
https://www.youtube.com/watch?v=XtN24GJyn4M 

Comunicación Profinet en TIA Portal: https://www.youtube.com/watch?v=6CcCDKXEx1g

Agregar ficheros GSD: https://www.youtube.com/watch?v=LJKUzv3Zykw

## Adquisición de archivos GSDML

Para localizar los archivos GSDML debemos acceder a la siguiente carpeta dentro del equipo que tenga el workvisual

- Dentro del disco C entra en la carpeta archivos de programa(x86)
- Busca la carpeta llamda KUKA
- Entramos en la carpeta WorkVisual 6.0
- Entras en la carpeta DeviceDescriptions

En esa carptera aparecerán todos los archivos GSDML que están disponibles para tu sistema en ese momento si necesitas uno que no aparece deberás descargarlos de la pagina oficial de KUKA. 

Para acabar copia la ruta de esa carpeta pues la necesitarás para añadir esos archivos a TIA Portal

## Añadir archivos GSDML a TIA Portal

El proceso comienza con la gestión de archivos de descripción de dispositivos dentro de TIA Portal en:

**OPCIONES → ADMINISTRAR ARCHIVOS DE DESCRIPCIÓN DE DISPOSITIVOS**

Desde esta ventana se selecciona la ruta donde se encuentran los archivos GSDML del fabricante y se instalan en el entorno. Una vez finalizada la instalación correctamente, el dispositivo pasa a estar disponible en el catálogo de hardware.

## Añadir KUKA a la vista de red

Después, en el catálogo de hardware, se busca el equipo correspondiente y se arrastra al proyecto para integrarlo en la red PROFINET junto con la CPU del PLC estando en la vista de redes.

En este caso, se configuró un dispositivo **KUKA KRC4-ProfiNet 4.0** y se enlazó con una **CPU 1215C** mediante un sistema **PROFINET IO**.

A continuación, se accede a la configuración del dispositivo para revisar:

- La interfaz PROFINET  
- Las direcciones Ethernet  
- Los parámetros de comunicación  

Finalmente, se utiliza la opción de **asignación de nombre de dispositivo PROFINET** para detectar el equipo físico en la red y sincronizarlo con la configuración del proyecto.

---

> ⚠️ **IMPORTANTE**  
> El procedimiento mostrado corresponde a un **KRC4**, mientras que en la práctica el sistema requerido era un **KRC5**.