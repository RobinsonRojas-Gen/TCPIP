# TCPIP

# 🌟 ¿Qué es TCP/IP?
TCP/IP es el conjunto de protocolos que hace posible Internet. Es como el "idioma" que hablan todos los dispositivos conectados a la red.

# 🎯 ¿Por qué es importante para desarrolladores web?
Cada vez que tu código hace una petición HTTP, envía datos a una base de datos, o conecta con una API, está usando TCP/IP. Entenderlo te ayuda a:

- Debuggear problemas de conexión
- Optimizar el rendimiento de aplicaciones
- Configurar servidores y bases de datos
- Entender la seguridad web

# 💡 Ejemplo práctico:
Cuando escribes fetch('https://api.github.com/users') en JavaScript, tu navegador:

- Resuelve la dirección IP de api.github.com
- Establece una conexión TCP en el puerto 443
- Envía una petición HTTP/HTTPS
- Recibe la respuesta JSON