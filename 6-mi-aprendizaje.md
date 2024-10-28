# COMPLETAR  
Comparando sus conocimientos antes de hacer la práctica con sus conocimientos después de hacer la tarea, explicar los principales aprendizajes logrados para beneficio de su formación profesional.  
Si solucionó un problema presentado o utilizó otros comandos que no se mencionan al realizar la práctica también se debe documentar.

Antes de realizar esta práctica, mi conocimiento sobre el uso y gestión de volúmenes en Docker era limitado. Aunque tenía una idea general por cuestiones de las anteriores practicas 1 y 2, desconocía la diferencia entre los tipos de volúmenes (volúmenes nombrados, anónimos y volúmenes de tipo host) y cómo cada uno se aplica en diferentes escenarios de desarrollo. A continuación, destaco los principales aprendizajes y beneficios para mi formación profesional.

1. Comprensión de los tipos de volúmenes en Docker
   Aprendí que los volúmenes anónimos, nombrados y de tipo host tienen usos específicos:
   - Volúmenes anónimos: son útiles para datos temporales, pero requieren ser manejados con cuidado ya que persisten solo mientras el contenedor existe y luego se vuelven difíciles de gestionar.
   - Volúmenes nombrados: permiten almacenar datos de manera persistente y se identifican fácilmente, por lo que pueden reutilizarse en distintos contenedores sin necesidad de especificar rutas exactas del sistema.
   - Volúmenes de tipo host: ofrecen un control total al usuario al vincular carpetas del sistema directamente en el contenedor, útil para mantener los archivos accesibles en el host y gestionarlos con facilidad.

2. Utilización de volúmenes en escenarios específicos
   La práctica me ayudó a comprender cómo gestionar la persistencia de datos en bases de datos y aplicaciones web como WordPress y Drupal, creando estructuras sólidas de almacenamiento y volúmenes para cada servicio. Aprendí a conectar contenedores en una misma red y asegurar la persistencia de datos mediante el uso adecuado de volúmenes, especialmente en escenarios de bases de datos donde la pérdida de información puede ser crítica.

3. Mejor manejo de comandos en Docker
   Además de los comandos comunes (`docker run`, `docker rm -fv`), adquirí experiencia en comandos útiles como `docker volume prune`, que permite limpiar los volúmenes anónimos no utilizados, liberando espacio en el sistema de manera eficiente. También practiqué el uso de `docker volume create` para nombrar volúmenes, y el uso de redes con `docker network create`, lo cual es esencial en la orquestación de contenedores para aplicaciones interconectadas.

4. Gestión de volúmenes en entornos WSL y Linux
   Aprendí sobre el acceso a los puntos de montaje de los volúmenes en el host, lo que facilita la depuración y supervisión de archivos almacenados en contenedores desde el sistema de archivos del host. El uso de `\\wsl.localhost\docker-desktop-data\data\docker\volumes` en entornos WSL es un conocimiento útil para manejar datos de contenedores en un sistema Windows.

### Problemas solucionados y comandos adicionales

Durante la práctica, me encontré con algunos problemas de permisos al acceder a volúmenes en el host. La solución fue verificar los permisos de las carpetas host y en algunos casos asignar permisos específicos. Además, utilicé el comando `docker inspect <nombre volumen>` para verificar el `Mountpoint` de los volúmenes, lo cual me ayudó a comprender mejor la ubicación física de los datos.

### Conclusión

Esta práctica consolidó mi comprensión sobre la persistencia de datos en Docker y cómo aplicarla en aplicaciones multi-servicio, un aprendizaje clave para mi para pasar la materia de Construccion y evolucion de software, tambien para el desarrollo profesional en la gestión de contenedores y despliegue de aplicaciones.


