# Privacidad de la beta Android/Wear

La app móvil usa la cuenta de LibreLinkUp que introduces para consultar las lecturas compartidas autorizadas. Guarda las credenciales cifradas con Android Keystore y mantiene estado e historial local para mostrar lecturas y gráficos. El reloj recibe estado/lecturas mediante Wear Data Layer y no recibe tu contraseña o token de LibreLinkUp. Las esferas consultan proveedores de la app Wear.

No se configura un servicio analítico propio ni un servidor GlucoTick para recibir lecturas. LibreLinkUp y los servicios de Google necesarios para Wear son servicios externos con sus propias condiciones. Data Layer puede usar Bluetooth o un transporte de Google según la conexión disponible.

Configura en Ajustes si el indicador y las notificaciones muestran detalles con el dispositivo bloqueado. Revocar permisos, cerrar sesión o desinstalar puede afectar seguimiento, avisos y datos guardados. El instalador de PC verifica APK, versión y firma y no extrae cuentas o lecturas; puede copiar temporalmente un APK instalado para comprobar su certificado.

No incluyas datos clínicos, credenciales o capturas personales en GitHub Issues. Para reproducir fallos utiliza DEMO. Esta documentación corresponde a la beta identificada en VERSION.json; no sustituye las condiciones de los servicios externos.
