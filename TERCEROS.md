# Componentes de terceros

GlucoTick conserva las licencias y avisos de sus dependencias. Esta lista se contrasta con el inventario de compilación; sus fuentes no se incorporan como código privado de GlucoTick.

- AndroidX, Jetpack Compose, Room, Core y bibliotecas Wear: Android Open Source Project / Google, licencia Apache2.0. https://github.com/androidx/androidx
- Kotlin, coroutines y kotlinx.serialization: JetBrains y colaboradores, licencia Apache2.0. https://github.com/JetBrains/kotlin y https://github.com/Kotlin/kotlinx.coroutines y https://github.com/Kotlin/kotlinx.serialization
- OkHttp y Okio: Square y colaboradores, licencia Apache2.0. https://github.com/square/okhttp y https://github.com/square/okio
- Guava ListenableFuture y JSpecify: anotaciones y utilidades transitivas, licencia Apache2.0. https://github.com/google/guava y https://github.com/jspecify/jspecify
- Public Suffix List: datos incluidos por OkHttp4.12.0, licencia Mozilla Public License2.0. El APK conserva el aviso de `okhttp3/internal/publicsuffix/NOTICE`. Datos y fuentes: https://publicsuffix.org/list/public_suffix_list.dat y https://github.com/publicsuffix/list; versión de OkHttp incluida: https://github.com/square/okhttp/tree/parent-4.12.0
- Google Play services Wearable: distribuido bajo las condiciones del SDK de Google Play services. https://developers.google.com/android/guides/overview
- Watch Face Format: plataforma Android/Wear; recursos propios GlucoTick validados con la herramienta oficial. https://developer.android.com/training/wearables/wff

Los avisos embebidos en META-INF y el aviso de Public Suffix List se conservan en los APK. Se incluyen los textos completos [Apache2.0](APACHE-2.0.txt) y [MPL2.0](MPL-2.0.txt). Son licencias de esos componentes y datos; no convierten el código privado de GlucoTick en código abierto.

FreeStyle Libre, LibreLinkUp, Abbott, Android y Wear OS son nombres de sus respectivos titulares. GlucoTick no es una app oficial de Abbott o Google.
