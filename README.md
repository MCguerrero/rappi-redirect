# rappi-redirect
<!DOCTYPE html>
<html lang="es">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Redirigiendo a Rappi...</title>
  <script type="text/javascript">
    window.onload = function() {
      var userAgent = navigator.userAgent.toLowerCase();
      var isMobile = /iphone|ipod|android/i.test(userAgent);
      
      if (isMobile) {
        // Intentamos abrir la app de Rappi
        window.location = "rappi://gbrappi/app/com.grability.rappi?goto=rappi_pay&section=cp_clabe";
        
        // Si la app no se abre, redirigimos a la página web de Rappi después de 1 segundo
        setTimeout(function() {
          window.location = "https://www.rappi.com/?goto=rappi_pay&section=cp_clabe";
        }, 1000);
      } else {
        // Si no es móvil, redirigimos directamente a la página web de Rappi
        window.location = "https://www.rappi.com/?goto=rappi_pay&section=cp_clabe";
      }
    };
  </script>
</head>
<body>
  <p>Redirigiendo...</p>
</body>
</html>
