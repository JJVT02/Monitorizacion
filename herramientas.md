# PROCESOS
ps: Muestra información de los procesos activos.

top: Proporciona una visión en tiempo real de los procesos que consumen más recursos,
como la CPU y la memoria.

htop: Similar a top, pero con una interfaz más visual y funciones adicionales, como la
capacidad de desplazarse y filtrar procesos de manera más intuitiva.
atop: Registra e informa de la actividad de todos los procesos del servidor.

# MEMORIA, ESPACIO Y RENDIMIENTO DEL DISCO
free: Muestra la cantidad de memoria libre y utilizada en el sistema.
df: Muestra el espacio utilizado y disponible en los sistemas de archivos montados.

du: Muestra el espacio ocupado por un fichero o directorio.

iostat: Se utiliza para rastrear los problemas de rendimiento de los dispositivos de
almacenamiento.

# TRÁFICO DE LA RED
tcpdump: Analiza el tráfico que circula por la red.
tcptrack: Nos muestra las conexiones establecidas, su origen, destino, estado, el tiempo
de iddle y la velocidad de transferencia.

iptraf: Intercepta paquetes en la red y muestra información sobre el tráfico.
bandwidthd: una herramienta específica de monitorización del ancho de banda

# PUERTOS
netstat (ss): Muestra las conexiones activas de una computadora, tanto entrantes como
salientes.

# Comandos sobre los procesos

```bash
ps
ps a
ps au
ps aux 
ps -C nano
ps aux | grep "nano"
ps -U alumno 
```

M memoria
p cpu
N

# Atop
- Guarda las estadisticas del sistema, empieza a tomar datos desde el momento en el que se instala
- servicio: systemctl status atop
- fichero: /etc/default/atop
- /var/log/atop_(fecha)
- atop -r /var/log/atop_(fecha)


# TCPDUM
tcpdump -n -i eno1 net 172.26.0.0/16  


1. Capturar todo el tráfico en una interfaz específica:

sudo tcpdump -i eth0

2. Filtrar por tipo de protocolo (ICMP):

sudo tcpdump -i eth0 icmp

3. Filtrar por dirección IP de origen o destino:

sudo tcpdump -i eth0 host 192.168.1.2

4. Filtrar por puerto (ejemplo: puerto 80 para tráfico HTTP):

sudo tcpdump -i eth0 port 80

5. Guardar la captura en un archivo:

sudo tcpdump -i eth0 -w capture.pcap

6. Mostrar datos en formato legible (ASCII):

sudo tcpdump -i eth0 -A

7. Filtrar por rango de direcciones IP:

sudo tcpdump -i eth0 net 192.168.1.0/24


# TCPTRACK

# IPTRAF

### Instalación de `iptraf` en Debian/Ubuntu:

```bash
sudo apt-get update
sudo apt-get install iptraf
```

Uso de iptraf:
Iniciar iptraf:

bash
Copy code
sudo iptraf
Monitorear el tráfico en tiempo real:

Selecciona "IP Traffic Monitor" para ver el tráfico por dirección IP.
Selecciona "General Interface Statistics" para obtener estadísticas generales de la interfaz.
Filtrar por interfaz:

Si tienes varias interfaces de red, puedes seleccionar la interfaz específica que deseas monitorear.
Salir de iptraf:

Puedes salir de iptraf presionando Q.

# Sistemas de monitorizacion
Nagios: es una herramienta de monitorización de código abierto que permite supervisar hosts, servicios y redes. Ofrece notificaciones, informes y visualizaciones a través de su interfaz web.


Zabbix: proporciona monitorización avanzada con capacidades de recopilación de datos, alertas, visualizaciones gráficas y más. Su interfaz web es robusta y fácil de usar.


Prometheus: es una solución de monitorización y alerta diseñada especialmente para entornos dinámicos. Ofrece almacenamiento local de series temporales y una interfaz web para consultas y visualizaciones.



