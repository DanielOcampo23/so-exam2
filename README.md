### Examen 2
**Universidad ICESI**  
**Curso:** Sistemas Operativos  
**Docente:** Daniel Barragán C.  
**Tema:** Namespaces, CGroups, LXC
**Correo:** daniel.barragan at correo.icesi.edu.co

### Objetivos
* Comprender los fundamentos que dan origen a las tecnologías de contenedores virtuales
* Conocer y emplear funcionalidades del sistema operativo para asignar recursos a procesos
* Conocer y emplear capacidades de CentOS7 para la virtualización

### Prerrequisitos
* Virtualbox o WMWare
* Máquina virtual con sistema operativo CentOS7

### Descripción
El segundo parcial del curso sistemas operativos trata sobre el manejo de namespaces, cgroups y virtualización por medio de LXC/LXD

### Solución
3. Para realizar la prueba de concepto primero tenemos que asegurarnos de que la maquina en la cual estamos trabajando tiene un solo nucleo para esto se evidencia en las siguientes imagenes




Después de esto se crean los scrips que estresaran el sistema mediante un ciclo infinito, para esto se crearán dos scripts llamados ```countA.sh``` y ```countB.sh``` con todos los permisos


Después de esto se tiene que crear como un servicio para poder ser ejecutado bajo systemd, para esto tenemos que ir a el directorio ```etc/systemd/system``` y dentro de esta carpeta crear ```countA.service``` y ```countB.service```



Y después de esto ejecutamos el comando ```systemctl daemon-reload``` para que el systemd vuelva a cargar todas las configuraciones nuevas que le hemos agregado, que son los dos nuevos servicios que creamos anteriormente mostrados. Después de esto verificamos con el comando ```systemctl status countA.service``` para verificar si se cargaron los servicios al sistema y si por el momento inactivo el servicio

(foto daemon )


Después corremos el servicio con el comando ```systemctl status countA.service``` y volvemos a verificar su estado para validar de que esté activo como lo mostrará la siguiente

(foto activo)




