##                                                                                          NGINX

### Nginx, pronunciado como “engine-ex”, es un servidor web de código abierto que, desde su éxito inicial como servidor web, ahora también es usado como proxy inverso, cache de HTTP, y balanceador de carga.

### Algunas compañías de alto perfil que utilizan Nginx incluyen Autodesk, Atlassian, Intuit, T-Mobile, GitLab, DuckDuckGo, Microsoft, IBM, Google, Adobe, Salesforce, VMWare, Xerox, LinkedIn, Cisco, Facebook, Target, Citrix Systems, Twitter, Apple , Intel, y muchos más (fuente).

### Nginx creado originalmente por Igor Sysoev, y tuvo su primer lanzamiento público en octubre de 2004. Igor concibió inicialmente el software como una respuesta al problema C10K, que se refiere al problema de rendimiento de manejar 10,000 conexiones concurrentes.

### Debido a que sus raíces yacen en la optimización del rendimiento bajo escala, Nginx a menudo supera a otros populares servidores web en pruebas de rendimiento (Benchmarks), especialmente en situaciones con contenido estático y/o un elevado número de solicitudes concurrentes, es por eso que Kinsta usa Nginx para impulsar su hosting.





## <p align="center">
## <h1>¿Cómo Funciona Nginx?</h1>
  <img src="https://www.techrepublic.com/a/hub/i/r/2017/09/28/3a9d4076-ba4c-4f6f-a5d8-161625cc8716/resize/770x/2db5d54233e54e1a7e45d1ce9a434cac/nginxhero.jpg">
</p>

### Nginx está diseñado para ofrecer un bajo uso de memoria y alta concurrencia. En lugar de crear nuevos procesos para cada solicitud web, Nginx usa un enfoque asincrónico basado en eventos donde las solicitudes se manejan en un solo hilo.

### Con Nginx, un proceso maestro puede controlar múltiples procesos de trabajo. El proceso maestro mantiene los procesos de trabajo, y son estos lo que hacen el procesamiento real.

### Algunas características comunes que se ven en Nginx incluyen:

   ### Proxy inverso con caché
   ### IPv6
   ### Balanceo de carga
   ### Soporte FastCGI con almacenamiento en caché
   ### Websockets
   ### Manejo de archivos estáticos, archivos de índice y auto indexación
   ### TLS / SSL con SNI
