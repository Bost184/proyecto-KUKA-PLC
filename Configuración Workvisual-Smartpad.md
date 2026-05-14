# Configuración para descargar el proyecto del SmartPad a WorkVisual

## Configuración de red en el PC

Para poder descargar proyectos en la aplicación WorkVisual, debemos seguir los siguientes pasos:

1. Entrar al **Panel de control** en el ordenador.
2. Acceder a **Centro de redes y recursos compartidos**.
3. Entrar en **Cambiar configuración del adaptador**.
4. Buscar la red **Ethernet** que esté estableciendo la comunicación entre el PC y el controlador KUKA.
    - El equipo debe estar conectado físicamente mediante cable Ethernet.
5. Acceder a **Propiedades** de la conexión.
6. Seleccionar **Protocolo de Internet versión 4 (TCP/IPv4)**.
7. Entrar en sus propiedades y configurarlo de la siguiente manera:
8. Activar: **Usar la siguiente dirección IP**
    - Dirección IP: 172.17.255.x
    - Sustituir la x por un valor entre 2 y 254
    - No usar:
        - 172.17.255.1 (dirección del controlador)
        - 172.17.255.0 (dirección de red)
        - 172.17.255.255 (broadcast)
        - Máscara de subred: 255.255.255.0
9. Puerta de enlace predeterminada: dejar en blanco
10. Aceptar los cambios y cerrar el Panel de control.

## Verificación de la conexión

Con esto, el PC queda configurado para poder comunicarse con el controlador.

Para comprobar que la comunicación está correctamente establecida:

1. Abrir la consola (cmd)

2. Ejecutar el comando:

    - ping 172.17.255.1

**Resultado esperado**

- Si todo va bien, el controlador responderá correctamente.
- Si no hay respuesta, puede deberse a:
    - Configuración de red incorrecta
    - Cable Ethernet dañado o desconectado
    - Firewall de Windows bloqueando la comunicación
    - Dirección IP del controlador diferente a 172.17.255.1

Nota: En caso de duda, verificar la IP del controlador desde el SmartPad (pero no cambiarlo).

## Descarga del proyecto desde WorkVisual

Una vez confirmada la comunicación:

1. Abrir WorkVisual
2. Ir a Archivo > Buscar proyecto
3. Si la comunicación funciona:
    - Aparecerá una celda disponible
    - Pulsar el botón "+" para ver los proyectos disponibles
    - Seleccionar el proyecto correspondiente al controlador

## Resultado

Con esto:

- Estarás visualizando la configuración actual del SmartPad
- Podrás empezar a trabajar sobre el proyecto