# Trabajo-de-investigaci-n
Simulador en línea de Raspberry Pi a Azure IoT Hub.
Objetivo:Investigar con el simulador en línea de Raspberry Pi a Azure IoT Hub funciona mediante la utilizacion de  investigaciones en internet
 La transformación digital trae consigo la llamada Industria 4.0, es decir, la integración de nuevas tecnologías como internet de las cosas, computación en la nube, sistemas integrados, robots, realidad aumentada, fabricación aditiva y seguridad de la información. El desarrollo de nuevas tecnologías que incluyen IoT, es un campo que se está desarrollando y con esto, la necesidad de crear aplicaciones y sistemas que involucren dichas tecnologías ha llamado la atención del mercado. Esta revolución podrá generar impacto en varias áreas de la industria, las telecomunicaciones, la electrónica, medicina e incluso agricultura. En relación con la agricultura, un área llamada Agricultura 4.0, las tecnologías habilitadoras de la industria 4.0 se aplican en el campo para mejorar la producción y la calidad de vida. Entre estas tecnologías, Cloud Computing e Internet of Things (IoT) son aspectos destacados y se pueden aplicar a la detección de cultivos, la agricultura de precisión y el monitoreo de las condiciones climáticas. Existe un interés especial en las estaciones meteorológicas automáticas, compuestas por sensores que pueden enviar información climática al agricultor, sin la necesidad de un monitoreo en el sitio, donde la información recopilada sobre el clima puede ayudar en la planificación y decisión de los cultivos. Este documento cubre el uso de un sensor de temperatura y presión y el envío de sus datos a la nube de Azure, su monitoreo en tiempo real y el uso de Power BI para visualización de datos. Para tener una plataforma de comunicación entre el sensor y el módulo IoT Hub, la placa de procesamiento Raspberry Pi 3B + se utiliza con sus recursos, capaz de monitorear y transmitir datos al usuario en tiempo real. A través de este trabajo, se logra una comunicación rápida entre el dispositivo del módulo IoT y los datos del sensor comunicados correctamente en la nube.

El desarrollo de Raspberry Pi es que necesitabas un dispositivo físico y hardware (sensores, botones, etc.) para desarrollar y probar completamente tus soluciones de Internet de las cosas (IoT). Muchos realmente no han visto esto como un problema, ya que implementar código en el dispositivo no es realmente tan difícil. Sin embargo, esto presenta otro problema al aprender por primera vez cómo desarrollar soluciones de IoT. Esto puede ser especialmente complicado cuando necesita comprar hardware para comenzar a aprender cómo desarrollar una solución de IoT con Microsoft Azure IoT Suite.
Microsoft ha anunciado esta semana la disponibilidad de un nuevo simulador en línea de Raspberry Pi que se ha añadido al Azure IoT Hub y que permite a los usuarios aprender los conceptos básicos de trabajar con una Raspberry Pi sin tener realmente ningún hardware delante de ellos. El simulador en línea es una excelente manera de prototipar proyectos para nuestras Raspberry Pi antes de comprar los componentes necesarios para crear el proyecto en la vida real. Microsoft explica que hay tres áreas principales en el simulador web de Raspberry Pi que toman la forma de:
• Área de montaje – El circuito predeterminado es que una Raspberry Pi se conecta con un sensor BME280 y un LED. El área está bloqueada en la versión preliminar, así que actualmente no se puede hacer la personalización. 
• Área de codificación: un editor de código en línea para codificar con una Raspberry Pi. La aplicación de muestra predeterminada ayuda a recopilar datos del sensor BME280 y los envía al concentrador de IoT de Azure. La aplicación es totalmente compatible con dispositivos Raspberry Pi reales. 
• Ventana de consola integrada: muestra la salida de tu código. En la parte superior de esta ventana, hay tres botones. Ejecutar: ejecuta la aplicación en el área de codificación. Restablecer: restablece el área de codificación en la aplicación de muestra predeterminada. Doblar / Expandir – En el lado derecho hay un botón para que usted pueda doblar / expandir la ventana de la consola.


El simulador en línea de Raspberry Pi Azure IoT se divide en las siguientes áreas de interfaz de usuario:

Ensamblaje de hardware: puede ver el estado de su dispositivo y su configuración de hardware
Editor de codificación: tiene acceso a un editor de código en línea para escribir su aplicación y ejecutarla en el dispositivo con Node.js.
Ventana de consola integrada: puede ver la salida de la consola de su aplicación aquí. 

Para aprenda los conceptos básicos del simulador en línea Raspberry Pi.

- Crea un centro de IoT.
- Registre un dispositivo para Pi en su centro de IoT.
- Ejecute una aplicación de muestra en Pi para enviar datos de sensores simulados a su centro de IoT.

Conecte Raspberry Pi simulado a un centro de IoT que cree. Luego ejecuta una aplicación de muestra con el simulador para generar datos del sensor. Finalmente, envía los datos del sensor a su centro de IoT.

Pasos a seguir 
- Cómo crear un centro de IoT de Azure y obtener la nueva cadena de conexión del dispositivo.
- Cómo trabajar con el simulador en línea Raspberry Pi.
- Cómo enviar datos del sensor a su centro de IoT.
-Descripción general del simulador web Raspberry Pi
-Haga clic en el botón para iniciar el simulador en línea Raspberry Pi.
-Iniciar simulador de Raspberry Pi

Descripción general del simulador en línea de Pi

1. Crear un centro de IoT
   En Azure Portal , haga clic en Nuevo > Internet de las cosas > IoT Hub .

2. Crear un iot hub en el portal de Azure

   En el panel del centro de IoT , ingrese la siguiente información para su centro de IoT:

Nombre : es el nombre de su centro de IoT. Si el nombre que ingresa es válido, aparece una marca de verificación verde.
Precios y nivel de escala : seleccione el nivel de F1 gratuito. Esta opción es suficiente para esta demostración. Ver precios y nivel de escala .
Grupo de recursos : cree un grupo de recursos para alojar el centro de IoT o use uno existente. Consulte Uso de grupos de recursos para administrar sus recursos de Azure .
Ubicación : seleccione la ubicación más cercana a usted donde se crea el centro de IoT.
Fije el tablero : marque esta opción para acceder fácilmente a su centro de IoT desde el tablero.
Complete los campos para crear su centro de IoT de Azure

3. Haz clic en Crear . Puede tomar algunos minutos para que se cree su centro de IoT. Puede ver el progreso en el panel de notificaciones .
Ver notificaciones del progreso de la creación de su centro de IoT

4. Una vez que se crea su centro de IoT, haga clic en él desde el tablero. Tome nota del nombre de host y luego haga clic en Políticas de acceso compartido .
Obtenga el nombre de host de su centro de IoT

5. En el panel Políticas de acceso compartido , haga clic en la política de iothubowner y luego copie y tome nota de la cadena de conexión de su centro de IoT. Para obtener más información, consulte Control de acceso a IoT Hub .
Obtenga su cadena de conexión del centro de IoT

Registre un dispositivo en el centro de IoT para su dispositivo

1. En Azure Portal , abra su centro de IoT.
2. Haz clic en Explorador de dispositivos .
3.En el panel Explorador de dispositivos, haga clic en Agregar para agregar un dispositivo a su centro de IoT.
    ID del dispositivo : la ID del nuevo dispositivo. Las ID de dispositivo distinguen entre mayúsculas y minúsculas.
    Tipo de autenticación : seleccione clave simétrica .
    Generar claves automáticamente : marque este campo.
    Conecte el dispositivo a IoT Hub : haga clic en Habilitar .
    Agregue un dispositivo en el explorador de dispositivos de su centro de IoT

4. Haz clic en Guardar .
5. Después de crear el dispositivo, ábralo en el panel Explorador de dispositivos .
6. Tome nota de la clave principal de la cadena de conexión. Obtenga la cadena de conexión del dispositivo

Ejecute una aplicación de muestra en el simulador web Pi

En el área de codificación, asegúrese de estar trabajando en la aplicación de muestra predeterminada. Reemplace el marcador de posición en la línea 15 con la cadena de conexión del dispositivo de Azure IoT Hub. Reemplace la cadena de conexión del dispositivo
Haga clic en Ejecutar o escriba npm startpara ejecutar la aplicación.
Debería ver la siguiente salida que muestra los datos del sensor y los mensajes que se envían a su centro de IoT Salida: datos del sensor enviados desde Raspberry Pi a su centro de IoT













