<!DOCTYPE html>
<html lang="es" class="dark">
  <head>
    <meta charset="UTF-8" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0, maximum-scale=1" />
    <title>Sobre la Vía – Navegación y Seguridad Vial</title>
    <meta name="description" content="App de navegación, seguridad y asistencia legal en carretera. 24/7 con botón de pánico, monitoreo en tiempo real y asistencia legal en carretera." />
    <!-- PWA Meta Tags -->
    <meta name="theme-color" content="#3B82F6" />
    <meta name="apple-mobile-web-app-capable" content="yes" />
    <meta name="apple-mobile-web-app-status-bar-style" content="black-translucent" />
    <meta name="apple-mobile-web-app-title" content="Sobre la Vía" />
    <link rel="manifest" href="/manifest.json" />
    <link rel="apple-touch-icon" href="/icon.svg" />
    <link rel="preconnect" href="https://fonts.googleapis.com" />
    <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin />
    <link href="https://fonts.googleapis.com/css2?family=Inter:wght@300;400;500;600;700;800;900&family=Roboto+Mono:wght@300;400;500;600;700&display=swap" rel="stylesheet" />
  </head>
  <body>
    <div id="root"></div>
    <script type="module" src="/src/main.tsx"></script>
    <!-- PWA Service Worker Registration -->
    <script>
      if ('serviceWorker' in navigator) {
        window.addEventListener('load', () => {
          navigator.serviceWorker.register('/service-worker.js')
            .then(registration => console.log('SW registrado:', registration.scope))
            .catch(error => console.log('Error SW:', error));
        });
      }
    </script>
  </body>
</html>
