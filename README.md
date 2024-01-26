# DETECCION DE OBJETOS CON ESP32 CAM | INTELIGENCIA ARTIFICIAL PYTHON + OpenCV + Yolov3 (EN TIEMPO REAL)

Hacer un git clone de la carpeta

https://github.com/davidcanoteayuda/esp32cam-IA.git

Abrir el archivo Wifi_ESP32cam.ino

Añadir url en las preferencias -> añadir a boards --> https://espressif.github.io/arduino-esp32/package_esp32_index.json

Hay que instalar Espressif system

# En arduino IDE

Seleccionamos la board esp32 -> ESP32WROVER Module
Flash Frecuency - 80Mhz
Flash mode - QIO
Partition Scheme - Huge APP (3mb)
Upload Speed - 921600

Pulsamos Upload

En la linea 7 hay que poner la direccion ip que nos asigna nuestro DHCP cuando metemos el arduino.

Se realiza con "coco.names" que se encuentra en el mismo directorio. 

En la parte de python se hace referencia en las lineas 13 al 26: donde se realiza la configuración y pesos de YoloV3 con la ayuda del modulo "dnn" de openCV. 

El archivo coco.names contiene los nombres de distintos objetos que se han entrenado para deteccion de objetos... Luego se almacena en "classNames".  y así como "net" se basa en usar librerías para para capas de calculo de salida, cargar y procesar que ya fueron implementados y más información se encuentra en Internet.

Ahora preparamos con Visual Studio Code la ejecucion.

instalamos con pip para crear entorno virtual 

pip install virtualenv

lo creamos

virtualenv venv

lo activamos

.\venv\Scripts\activate

instalamos opencv

pip install opencv-python

instalamos numpy

pip install numpy

Ejecutamos el archivo y movemos la camara para ver que detecta objetos

.\IPaddressClassification.py

