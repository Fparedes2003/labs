Lab 3: Protocolos de Comunicación Seguros (Habilidad: Tráfico e Intercepción)
Entorno: Kali (Wireshark) y un servidor Apache/Nginx

Actividad: Análisis de tráfico inseguro vs. cifrado.
Herramientas: Wireshark, Certbot (Let's Encrypt), OpenVPN/WireGuard.
Tarea: Capturar una sesión HTTP y ver la contraseña en texto plano. Luego, configurar un certificado SSL (HTTPS) y verificar que el tráfico ahora es ilegible. Configurar un túnel SSH con llaves deshabilitando el acceso por contraseña.

Dinámica:
Sniffing de HTTP: El alumno llena un formulario en una web HTTP mientras corre Wireshark. Verá su usuario y contraseña en texto plano (filtro http.request.method == "POST").

Hardening con SSH Tunneling: Aprender a crear un túnel local para proteger tráfico inseguro.
ssh -L 8080:localhost:80 usuario@servidor

¿QUE SE HARA?

En este laboratorio se levantara una pagina con ubuntu server con apache esta pagina será modificada con un formulario simple el cual usara del método http post. Luego de la configuración de la pagina desde la maquina atacante se entrara, se ingresaran las credenciales y se enviara el formulario. Desde la misma maquina atacante se iniciara wireshark para poder visualizar el trafico y ver si es posible capturar las credenciales en texto plano.

Para evitar esto se creara un túnel ssh el cual deberá ser solo ingresado mediante la clave de una llave la cual será creada en este laboratorio, también, se incorporara y configurara un certificado ssl para obtener https y de esta manera evitar que las credenciales del usuario se vean a través de wireshark en texto plano.

¿QUE SE VERA?

Se podrá ver lo insegura que es una pagina sin certificado ssl debido a la facilidad que hay en el que sea interceptada con herramientas como wireshark.

También vera la configuración y creación de un túnel ssh y el certificado ssl junto con la utilización de la herramienta wireshark.

FINALIDAD

Implementar herramientas y protocolos de protección para lograr una comunicación segura mediante cifrado.

HERRAMIENTAS

-Wireshark

-Apache

-ssl

-ssh

-Kali Linux

-Ubuntu Server

