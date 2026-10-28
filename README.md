# Zenith Capture

Captura planetaria y lunar para el ecosistema Zenith Astro Code.

[Descargar instaladores y actualizaciones](https://github.com/eduardomg1499/zenith-capture/releases/latest) · [Zenith Astro Code](https://www.zenith-astro.com)

Este repositorio contiene instaladores públicos y el manifiesto de actualización. El código y los asistentes de publicación se mantienen en el repositorio privado de desarrollo.

## macOS

Requiere macOS 13.3 o posterior. Abre el DMG y arrastra la app a Aplicaciones.

| Archivo | Equipo y SDK |
| --- | --- |
| `*_aarch64.dmg` | Apple Silicon, AVFoundation y SDK compatibles con ARM64. |
| `*_x86_64.dmg` | Intel; Apple Silicon con Rosetta para SDK Intel, incluidos los actuales de SVBONY, ASI y QHY. |

Los paquetes macOS usan firma Developer ID, runtime endurecido, notarización de Apple y ticket incorporado. No desactives Gatekeeper. Los SDK propietarios de cámaras se instalan por separado; revisa [la guía macOS](LEEME-macOS.md). La versión inicial se publica para pruebas de campo; la compatibilidad física depende de cada modelo, SDK y arquitectura.

`SHA256SUMS` permite verificar las descargas. Los archivos `*.app.tar.gz` y sus firmas se destinan al actualizador integrado. Para instalar manualmente utiliza los DMG.

## Windows

El instalador de Windows se añadirá a la misma publicación cuando termine su compilación y verificación. El manifiesto conserva ambas arquitecturas macOS al añadir Windows.

## Retroalimentación

Dentro de la app abre **Soporte y diagnóstico**. Puedes describir el problema, revisar el informe, autorizar su exportación y guardar un JSON para adjuntarlo a tu reporte. El informe reúne errores y contexto de compatibilidad, oculta datos sensibles y no incluye tus imágenes. No se envía automáticamente; tú decides compartirlo.

Al reportar indica los pasos, el resultado esperado y lo que ocurrió, además del modelo de cámara/accesorio y el archivo de diagnóstico si autorizas compartirlo.
