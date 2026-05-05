Lab 2: Ataque y Defensa de Credenciales (Habilidad: Gestión de contraseñas)

Actividad: Realizar ataques de diccionario y fuerza bruta, para luego implementar MFA.
Herramientas: Hydra, John the Ripper, Google Authenticator PAM module.
Tarea: Romper una contraseña débil de SSH usando Hydra. 
Luego, instalar y configurar el módulo de Google Authenticator en el servidor Ubuntu para que, aunque el atacante tenga la clave, no pueda entrar sin el token.

Dinámica:
Fase de Ataque: Desde Kali, usar Hydra para realizar un ataque de diccionario contra el servicio SSH del Ubuntu.
hydra -l usuario -P lista_passwords.txt ssh://[IP_Servidor]
Fase de Hardening (MFA): En el Ubuntu Server, instalar el módulo PAM de Google Authenticator.
sudo apt install libpam-google-authenticator
Ejecutar google-authenticator y configurar la App en el celular.
Configuración de SSH: Modificar /etc/pam.d/sshd y /etc/ssh/sshd_config para exigir tanto la contraseña como el token (MFA).
Prueba Final: Volver a intentar el ataque con Hydra. Aunque Hydra encuentre la contraseña, la conexión fallará porque no puede saltarse el segundo factor.



