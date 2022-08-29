# Flow-3
En este repositorio se encuentra explicado el ejercicio 3 con Node Red, el cual consiste en observar la fecha y hora mediante el uso de dashboards.

## Material necesario
Para poder realizar necesario es necesario tener instalado:
- [Node.js](https://github.com/nodesource/distributions/blob/master/README.md) Usar la versión LTS v16x e instalar los build tools.
- [Node-Red](https://nodered.org/docs/getting-started/local)
- [Ubuntu 20.04](https://ubuntu.com/download/desktop/thank-you?version=20.04.2.0&architecture=amd64)

## Material de referencia
Para hacer las instalaciones requeridas para este ejercicio se siguieron los pasos de los cursos siguientes:
- [Instalación de Ubuntu 20.04 en VirtualBox Windows](https://edu.codigoiot.com/course/view.php?id=812)
- [Instalación de NodeRed en Ubuntu 20.04](https://edu.codigoiot.com/course/view.php?id=817)
- [Introducción a NodeRed](https://edu.codigoiot.com/course/view.php?id=278)

## Instrucciones
1. Abrir la terminal y escribir el siguiente comando: **node-red**.
>Nota: Es importante escribir este comando en la terminal ya que si no se hace no se podrá trabajar con Node Red.
2. En el navegador escribir: **localhost:1880**, se abrirá Node Red.
3. Colocar el bloque de **inject** y el bloque de **debug**. 
4. Dar doble click al bloque de **inject** y en donde dice "repeat" seleccionar la opción de *interval* y colocar un tiempo de un segundo.
5. Agregar un bloque **function** y copiar el siguiente código:
>var date = new Date(msg.payload);
>msg.payload = date.toString();
>return msg;
6. Una vez copiado dar click en el botón **Done**.
7. Unir el bloque **function** con el bloque **inject** y el bloque **debug**.
8. En la esquina superior derecha de Node Red aparecen 3 líneas, al darles click se desplegará un menú, buscar la opción de *Manage palette* y dar click.
9. Se desplegará una ventana con el título de *User settings*, dar click en la ventana *Install* y buscar el módulo llamado **node-red-dashboard*, instalarlo.
10. Una vez instalado, buscar el bloque **text** y unirlo a la salida del bloque **function**.
11. Para configurar el bloque text, en la pantalla que se despliega del lado derecho, buscar la opción de dashboard y agregar un nuevo tab.
12. En el tab agregar un nuevo grupo y dar click en *update*.
13. Configurar el bloque **text** seleccionando el grupo anteriormente creado y añadiendo una descripción para señalar la hora y fecha.
15. Finalmente, dar click en el botón **Deploy** para que se actualicen los cambios. 

## Resultados
Una vez completados los pasos anteriores se deberá ver abrir el dashboard, como se muestra a continuación:

![Captura de pantalla](Captura_Flow3.png)

![Captura de pantalla](Captura_bloques.png)

## Evidencias
[Evidencia Flow 3](https://youtu.be/1KQllEilVR0)

## Créditos
Este ejercicio fue basado en los ejercicios que se encuentran en el repositorio [flow3-NodeRed](https://github.com/hugoescalpelo/Flow3-NodeRed)

Documentación realizada por [Karen Rosas](https://github.com/KarenRosas49)