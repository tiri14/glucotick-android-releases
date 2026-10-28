# Instalación de GlucoTick Android/Wear — 0.1.14-beta.1

Descarga oficial: https://github.com/tiri14/glucotick-android-releases/releases/tag/android-v0.1.14-beta.1. Comprueba SHA256SUMS.txt. El ZIP incluye siete APK, VERSION.json, guías y el instalador; los APK individuales están identificados por Android, WearOS y nombre de esfera.

## Móvil

Requiere Android8 o posterior. Abre el APK Android en el teléfono y autoriza la instalación desde esa fuente cuando Android lo solicite. Conecta una cuenta autorizada de LibreLinkUp, selecciona la persona compartida y pulsa Iniciar seguimiento. Concede notificaciones si quieres el indicador/avisos. Revisa la exención de batería del fabricante y configura privacidad y frecuencia desde Ajustes.

## Reloj y esferas

Requieren Wear OS4/API33 o posterior y emparejamiento normal con un móvil admitido por el fabricante y su acompañante; el mínimo del APK móvil no garantiza todas las combinaciones de emparejamiento. Activa depuración según las instrucciones de tu reloj y usa ADB de [Platform Tools oficial](https://developer.android.com/tools/releases/platform-tools). La beta GitHub necesita instalación separada en el reloj; no es una instalación desde Play.

Con el ZIP extraído en Windows PowerShell, comprueba primero:

```powershell
.\INSTALAR.ps1 -VerifyOnly
```

Si PowerShell bloquea la ejecución del script, permite ejecutarlo solo en esa ventana con `Set-ExecutionPolicy -Scope Process -ExecutionPolicy Bypass -Force` y repite el comando. Al cerrar la ventana termina ese permiso temporal; no es necesario cambiar la política del equipo.

Instala solo en los destinos que indiques; usa las series que devuelve `adb devices`:

```powershell
.\INSTALAR.ps1 -AdbPath C:\PlatformTools\adb.exe -PhoneSerial SERIE_MOVIL
.\INSTALAR.ps1 -AdbPath C:\PlatformTools\adb.exe -WatchSerial SERIE_RELOJ -Faces All
```

Puedes elegir una lista de esferas, por ejemplo `-Faces Original,Dashboard`. Sin `-Faces` no instala esferas. `-WatchSerial` instala también la app Wear. Selecciona luego la esfera desde el selector normal del reloj. No confundir APK WearOS y APK Android: ambos pertenecen a la misma familia, con binarios para dispositivos diferentes.

## Actualizar y conservar datos

Solo se permite actualizar una instalación con la misma firma y versión compatible. La firma pública SHA-256 es `7f769c9fcf09e2b5333e729259b6359e0cd03565ae84f4e9e8dbbae514cb1478`. El instalador comprueba todos los destinos antes de la primera instalación y rechaza firmas distintas o versiones inferiores. Un corte durante la instalación puede dejar algunos componentes actualizados: revisa los mensajes y repite la instalación compatible; nunca borra datos para intentar resolverlo.

Las versiones privadas/debug anteriores no se sustituyen directamente. Conserva esa instalación y utiliza la beta de producción en otro entorno; la migración personal no forma parte de esta entrega. No publiques datos de cuenta ni copies almacenes cifrados entre firmas esperando que se descifren.

Al terminar, abre GlucoTick en el móvil y pulsa Iniciar seguimiento. Compara la lectura del reloj con el móvil y comprueba edad y estado. La beta no añade un actualizador automático ni garantiza reanudación al reiniciar. Si el seguimiento estaba detenido voluntariamente, permanece detenido hasta que lo inicies.

## Fallos frecuentes y retirada

- Sin lecturas: comprueba primero LibreLinkUp, invitación aceptada, selección y conexión de Internet del móvil.
- Sin datos en reloj: comprueba emparejamiento, ambas apps y que sus firmas coincidan. Las esferas necesitan la app Wear para sus proveedores.
- Esfera con solo hora y batería, sin glucosa: comprueba que también esté instalada la app **GlucoTick WearOS**. El APK de la esfera por sí solo no recibe lecturas. La app Wear puede funcionar sin instalar nuestras esferas; en una instalación vacía muestra que no hay datos ni recepción del móvil.
- Dispositivo no autorizado: desbloquea y acepta la autorización de depuración en el dispositivo correspondiente; el instalador no elimina ese bloqueo.
- Indicador ausente: revisa notificaciones, ocultación y privacidad en Ajustes. La ubicación la decide Android/One UI.
- Para retirar la beta, usa la desinstalación normal de Android/Wear. Desinstalar puede borrar datos, cuenta y configuración de widgets. Las esferas se retiran por separado. No afecta a GlucoTick Windows.
