# IPV - Proyecto Android

Este paquete contiene la aplicación web y la configuración inicial de Capacitor para generar una APK Android.

## Requisitos
- Node.js LTS
- Android Studio con Android SDK
- Java/JDK compatible con la versión de Android Gradle Plugin instalada por Capacitor

## Generar el proyecto Android
Desde esta carpeta, abre una terminal y ejecuta:

```bash
npm install
npx cap add android
npx cap sync android
npx cap open android
```

En Android Studio:
1. Espera a que termine la sincronización de Gradle.
2. Selecciona **Build > Build Bundle(s) / APK(s) > Build APK(s)**.
3. Android Studio mostrará la ubicación de la APK generada.

## Notas
- La aplicación carga los archivos incluidos en `www`; no depende de que Netlify esté disponible.
- Los datos del sistema se guardan con `localStorage` en el almacenamiento de la aplicación.
- Desinstalar la APK puede borrar esos datos. Conviene exportar/copiar respaldos periódicamente.
- El HTML original se ha conservado; se añadieron el manifiesto, el service worker y los iconos.
