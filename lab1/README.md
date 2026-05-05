Laboratorios Prácticos (Entorno Kali / Ubuntu)

Entorno: Ubuntu Server (Víctima/Servidor) y Kali (Auditor).

Actividad: Configuración de firma digital y verificación de integridad.
Comandos clave: openssl, sha256sum, gpg.
Tarea: Los alumnos deben generar un par de llaves (Pública/Privada), firmar un archivo de configuración crítico y verificar que si se cambia un solo bit del archivo, el hash de integridad falla.
Enfoque organizacional: Simular la firma de un manifiesto de software antes de subirlo a producción.


Dinámica:
Generación de Hash crea un archivo config_bancaria.txt. Usa sha256sum para generar su huella digital.
Simulación de Ataque: Un "atacante" modifica un solo carácter (ej: cambia un 0 por un 1 en un monto).
Verificación: El alumno vuelve a correr el hash y nota que la "huella" es totalmente distinta.
Firma Digital (OpenSSL):
Generar llave privada: openssl genrsa -out privada.pem 2048
Generar llave pública: openssl rsa -in privada.pem -pubout -out publica.pem
Firmar archivo: openssl dgst -sha256 -sign privada.pem -out firma.bin config_bancaria.txt



