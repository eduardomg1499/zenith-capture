# Zenith Capture para macOS

Versión inicial 0.1.0 para pruebas de campo. Requiere macOS 13.3 o posterior.

- **aarch64**: versión nativa para Apple Silicon. AVFoundation y los SDK con biblioteca ARM64 compatible.
- **x86_64**: versión para Intel. También funciona con Rosetta en Apple Silicon y es la opción para los SDK Intel actuales de SVBONY, ZWO ASI y QHY.

Abre el DMG y arrastra Zenith Capture a Aplicaciones. Ejecuta una sola versión a la vez. La aplicación y el DMG están firmados con Developer ID, notarizados por Apple y llevan el ticket de notarización incorporado. No es necesario desactivar Gatekeeper.

Los SDK propietarios de cámaras no se redistribuyen dentro del instalador. Si tu cámara necesita uno, obtén el SDK de su fabricante y coloca sus bibliotecas y dependencias en `~/Zenith/sdk` (dentro de tu carpeta de usuario). Los nombres principales son `libSVBCameraSDK.dylib`, `libASICamera2.dylib`, `libqhyccd.dylib` y `libPlayerOneCamera.dylib`. Deben coincidir con la arquitectura del paquete. Reinicia y usa Buscar cámaras; consulta el diagnóstico de compatibilidad si la biblioteca o una dependencia no carga. Para otras ubicaciones se admiten `ZENITH_SDK_DIR` o las variables específicas del fabricante al lanzar desde Terminal. No modifiques el interior de la app firmada. La compatibilidad depende del SDK, su arquitectura, el modelo, el cable y los permisos; esta publicación no acredita pruebas físicas de todos los dispositivos.

La app solicita permiso de cámara y de red local cuando esas funciones lo requieren. El runtime está endurecido; permite cargar bibliotecas de fabricantes externos para los SDK de cámaras, sin permitir JIT ni memoria ejecutable sin firma.

Para reportar un problema, abre **Soporte y diagnóstico**, revisa el contenido, marca el consentimiento y exporta el JSON. Tú decides cómo compartirlo. No se envía automáticamente y no incluye imágenes de captura. Describe los pasos y adjunta ese archivo a tu reporte.

Las actualizaciones se descargan del repositorio público y requieren una firma de actualización de Zenith Capture. Antes de instalar, detén el preview, las operaciones y desconecta los accesorios. Los archivos SHA256SUMS permiten comprobar la integridad de las descargas.
