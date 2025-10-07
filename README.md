# IoT Controller
Una aplicación móvil en Flutter para controlar un sistema IoT con Arduino a través de Bluetooth Clásico.

## Requisitos
- Flutter SDK (versión estable)
- Android Studio o Visual Studio Code con las extensiones de Flutter y Dart
- Dispositivo Android con Bluetooth habilitado
- Placa Arduino (o similar)
- Módulo Bluetooth HC-05 o HC-06
- Arduino IDE para subir el código al microcontrolador

## Configuración del Hardware
1.  **Conecta el módulo HC-05/06 al Arduino**:
    - VCC al 5V
    - GND a GND
    - RX a pin digital 11 del Arduino (a través de un divisor de voltaje si es necesario)
    - TX a pin digital 10 del Arduino
2.  **Sube el código**:
    - Abre el archivo `bluetooth_connection_test.txt` con el IDE de Arduino.
    - Asegúrate de que las librerías `SoftwareSerial` estén disponibles.
    - Conecta el Arduino, selecciona la placa y el puerto, y sube el código.

## Configuración del Software (Flutter)
1.  **Clona el repositorio**:
    ```bash
    git clone [https://github.com/](https://github.com/)[TU_USUARIO]/[NOMBRE_DEL_REPOSITORIO].git
    cd [NOMBRE_DEL_REPOSITORIO]
    ```
2.  **Instala las dependencias**:
    ```bash
    flutter pub get
    ```
3.  **Ejecuta la aplicación**:
    - Conecta tu dispositivo Android.
    - Habilita el Bluetooth en tu dispositivo móvil.
    - Asegúrate de que el Arduino y el HC-05/06 estén encendidos.
    - Ejecuta la aplicación desde tu IDE o terminal:
    ```bash
    flutter run
    ```

## Uso de la Aplicación
1.  En la pantalla principal, presiona **"Scan for Devices"**.
2.  Selecciona el módulo Bluetooth HC-05/06 de la lista.
3.  Una vez conectado, usa los botones **"Turn LED ON"**, **"Turn LED OFF"**, **"Send PING"** y **"Request STATUS"** para interactuar con la placa Arduino.
4.  Observa las respuestas en la consola de depuración de tu IDE.
5.  Presiona **"Disconnect"** para cerrar la conexión.
