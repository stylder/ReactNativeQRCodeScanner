# ReactNativeQRCodeScanner

<p align="center">
Este es un ejemplo de escáner de código de barras y código QR usando la cámara en React Native . Para hacer un escáner de código de barras y código QR en React Native vamos a utilizar una biblioteca muy buena proporcionada por Wix named  react-native-camera-kit. Esta biblioteca es muy fácil de integrar y el rendimiento para escanear el código de barras o QR Code es muy bueno.
</p>

<p align="center">
  <a href="https://github.com/stylder">
    <img alt="Made by Santiago García Cabral" src="https://img.shields.io/badge/made-by%20Santiago%20Garc%C3%ADa%20Cabral-green">
  </a>

  ![example app](/docs-assets/img1.jpg)

 ![example app](/docs-assets/img1.jpg)
</p>

## APK ejemplo
[Descargue el ejecutable aquí](/docs-assets/app-release.apk)

## Código de barras v / s Código QR
Un código de barras fue el primero en llegar al mercado para almacenar números pequeños y la representación de la información es de una dimensión.
<p align="center">

![example app](/docs-assets/barcode.gif)
<p>

El código QR es la versión actualizada del código de barras y almacena más información que el código de barras y la representación de la información tiene 2 dimensiones.
<p align="center">

![example app](/docs-assets/qr_example.PNG)

<p>


Si está creando una aplicación que necesita compartir un pequeño código / datos / URL entre usuarios en presencia física, entonces el código QR es lo mejor para integrar en su aplicación.

UPI o las aplicaciones de transacciones de pago son el ejemplo común en el que un usuario muestra el Código QR y el otro usuario escanea el Código QR para iniciar el pago. Si tiene la misma utilidad que necesita para crear el código QR, puede seguir el ejemplo para  generar el código QR en la aplicación React Native .

En este ejemplo, creará el escáner de código de barras y código QR utilizando React Native Camera. Haremos una pantalla de inicio con un botón para abrir el escáner de código de barras y código QR, esto abrirá una cámara con la funcionalidad de código de barras y escaneo QR y después de escanear el código de barras o código QR, llevaremos los datos a la pantalla de inicio y mostraremos allí.

Si los datos escaneados serán una URL, mostraremos un botón adicional para abrir la URL en el navegador predeterminado usando React Native Linking Component. Entonces empecemos.

## Para hacer una aplicación React Native
Comenzar con React Native lo ayudará a saber más sobre la forma en que puede hacer un proyecto React Native. Vamos a utilizar react-native init para crear nuestra aplicación React Native. Suponiendo que tiene un nodo instalado, puede usar npm para instalar la react-native-cliutilidad de línea de comando. Abra la terminal y vaya al espacio de trabajo y ejecute.

```javascript
npm install -g react-native-cli
```

Ejecute los siguientes comandos para crear un nuevo proyecto React Native

```javascript
react-native init ProjectName
```

## Instalación de dependencia
Para hacer el escáner de código de barras y código QR vamos a utilizar un CameraKitCameraScreen componente de la  react-native-camera-kit biblioteca. Para instalar esta biblioteca, abra la terminal y salte a su proyecto

```javascript
npm install react-native-camera-kit --save
```

## Instalación de CocoaPods
Después de la actualización de React Native 0.60, han introducido el enlace automático, por lo que no necesitamos vincular la biblioteca, pero necesitamos instalar pods. Entonces, para instalar pods, use

```javascript
cd ios && pod install && cd ..
```

## Permiso para usar la cámara para Android

Estamos usando una cámara API nativa para escanear el código de barras y el código QR, por lo que debemos agregar permiso al AndroidManifest.xmlarchivo para acceder a él.

Agregue los siguientes permisos en su AndroidMnifest.xml. Vaya a QR ScannerExample
> android -> aplicación -> principal -> AndroidMnifest.xml.

```javascript
<uses-permission android:name="android.permission.CAMERA"/>
```
## Para ejecutar la aplicación React Native
Para ejecutar el proyecto en un dispositivo virtual Android o en un dispositivo de depuración real
```javascript
react-native run-android
```

