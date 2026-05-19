Lab 1. Practica de defensa activa

Gestión de Parches y Hardening (Habilidad: Implementar parches)
Entorno: Ubuntu Server desactualizado.
Actividad: Los alumnos reciben un informe de vulnerabilidades (simulado).
Tarea: 1. Identificar servicios vulnerables usando nmap --script vuln. 2. Aplicar parches específicos usando apt-get install --only-upgrade [paquete]. 3. Configurar Unattended Upgrades para automatizar parches críticos.

Entorno: Una VM Ubuntu Server "congelada" en una versión antigua o con servicios vulnerables (ej. un servicio de impresión o una versión de OpenSSH con vulnerabilidades conocidas).
Dinámica:
Escaneo Inicial: Desde Kali, usar nmap -sV --script vuln [IP_Ubuntu]. Los alumnos deben identificar al menos 3 vulnerabilidades con su código CVE correspondiente.

Investigación: Buscar en la base de datos del NVD (NIST) qué permite hacer ese CVE (ej. RCE o DoS).

Aplicación de Parche:
Simular la política de "parches críticos primero".
Uso de apt-get install --only-upgrade [servicio] para no romper dependencias globales.

Configuración de Seguridad Autónoma: Instalar unattended-upgrades.
sudo apt install unattended-upgrades
Configurar /etc/apt/apt.conf.d/50unattended-upgrades para que solo se instalen parches de "Security".
Habilidad ganada: Capacidad de priorizar la remediación basada en el impacto organizacional.

¿QUE SE VA HACER?

Se utilizara una maquina ubuntu server desactualizada con el objetivo de identificar las vulnerabilidades que esta presenta, para posteriormente realizar una remediacion aplicando parches de seguridad.

Tambien se investigaran al menos 3 CVE detectados en la maquina victima para poder verificar cuales son los peligros que este representa para el sistema.

LO QUE SE VERA

Se lograran observar multiples servicios y sus vulnerabilidades, 

