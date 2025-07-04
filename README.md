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

# 🌐 TCP/IP vs OSI: Modelos de Red Comparados

## 📚 Tabla Comparativa

| Capa TCP/IP       | Capa OSI          | Protocolos Clave          | Funcionalidad Principal          |
|-------------------|-------------------|---------------------------|-----------------------------------|
| **Aplicación**    | Aplicación        | HTTP, FTP, DNS, SMTP      | Interfaz usuario-red              |
|                   | Presentación      | SSL, JPEG, MPEG           | Traducción y cifrado de datos     |
|                   | Sesión            | NetBIOS, RPC              | Control de diálogos               |
| **Transporte**    | Transporte        | TCP, UDP                  | Transferencia extremo a extremo   |
| **Internet**      | Red               | IP, ICMP, ARP             | Enrutamiento y direccionamiento   |
| **Acceso Red**    | Enlace de Datos   | Ethernet, PPP, Frame Relay| Direccionamiento físico (MAC)     |
|                   | Física            | RJ45, WiFi, Fibra Óptica  | Transmisión binaria               |

## 🏆 ¿Por qué TCP/IP domina Internet?

### ✅ Ventajas Clave
1. **Histórica**: Nació con ARPANET (predecesor de Internet)
2. **Eficiencia**: Modelo de 4 capas más simple que OSI
3. **Flexibilidad**: Soporta TCP (orientado a conexión) y UDP (sin conexión)
4. **Ubicuidad**: Todos los dispositivos modernos lo implementan

### 🔧 Arquitectura Práctica
- **Menos capas** → Más fácil de implementar
- **Capas amplias** → Mayor flexibilidad en protocolos
- **Enfoque end-to-end** → Ideal para redes heterogéneas

## 📖 Para Aprender Más
- `RFC 1122` (Especificación oficial TCP/IP)
- `IEEE 802.3` (Estándar Ethernet)
- `ISO/IEC 7498-1` (Modelo OSI original)

> 💡 **Dato curioso**: Aunque OSI no se usa directamente, su terminología (como "capa 2" o "capa 3") sigue siendo común en networking.

## 📊 Diagrama Conceptual

Internet (TCP/IP)
├─ Aplicación ≈ (OSI: Aplicación+Presentación+Sesión)
├─ Transporte ≈ Transporte
├─ Internet ≈ Red
└─ Acceso Red ≈ (Enlace de Datos+Física)

[🔼 Volver al inicio](#-tcpip-vs-osi-modelos-de-red-comparados)

# 🌐 El Modelo TCP/IP: Las 4 Capas Fundamentales

El modelo TCP/IP es la arquitectura que hace posible internet. Está compuesto por cuatro capas que trabajan juntas para enviar información de un lugar a otro:

## 1. 📱 Capa de Aplicación
Es la capa que ves y usas todos los días. Aquí viven las aplicaciones que conoces como navegadores web, WhatsApp, Instagram, Netflix y tu correo electrónico. Los protocolos principales incluyen HTTP/HTTPS para sitios web 🌍, SMTP para emails 📧, FTP para transferir archivos 📁 y DNS para convertir nombres de sitios web en direcciones numéricas 🔍. Esta capa presenta la información de manera que puedas entenderla y interactuar con ella.

## 2. 🚚 Capa de Transporte
Funciona como un servicio de paquetería confiable. Toma tus datos y los divide en paquetes más pequeños, asegurándose de que lleguen completos y en orden al destino 📦. Utiliza dos protocolos principales: TCP, que es como un servicio de entrega certificado que confirma que todo llegó bien ✅, y UDP, que es más rápido pero no garantiza la entrega, como enviar una postal 📮. También gestiona múltiples conversaciones simultáneas entre aplicaciones.

## 3. 🗺️ Capa de Internet
Es el GPS de internet. Su trabajo es encontrar la mejor ruta para que tus datos viajen desde tu dispositivo hasta su destino, pasando por múltiples redes y routers 🛤️. El protocolo IP es fundamental aquí, asignando direcciones únicas a cada dispositivo conectado (como direcciones de casa 🏠) y decidiendo qué camino deben seguir los paquetes de datos para llegar a su destino final.

## 4. 🔌 Capa de Acceso a Red
Representa la conexión física real entre dispositivos. Incluye todo el hardware que puedes tocar: cables de red, tarjetas de red, switches, routers y antenas WiFi 📡. También maneja los protocolos que controlan cómo se transmiten físicamente los datos. Gestiona tecnologías como Ethernet para conexiones por cable 🔗, WiFi para redes inalámbricas 📶, Bluetooth para dispositivos cercanos 📲, y otros métodos de conexión física.

# 🎯 Analogía Simple
Imagina enviar una pizza a domicilio 🍕:

Capa de Aplicación 📱: La app donde pides la pizza
Capa de Transporte 🚚: El repartidor que asegura que llegue completa
Capa de Internet 🗺️: El GPS que encuentra la ruta a tu casa
Capa de Acceso a Red 🛣️: Las calles y el vehículo que transportan físicamente la pizza

¡Así es como tus datos viajan por internet! ⚡

# 🔢 Direcciones IP: Tu Dirección en Internet
Las direcciones IP son como las direcciones postales de internet. Cada dispositivo necesita una para comunicarse.

## IPv4
Formato: 192.168.1.1

4 números del 0 al 255 separados por puntos

Problema: Solo hay ~4.3 mil millones de direcciones posibles

## IPv6
Formato: 2001:0db8:85a3::8a2e:0370:7334

8 grupos de 4 dígitos hexadecimales

Ventaja: Prácticamente infinitas direcciones

## IP Privada
Ejemplos: 192.168.x.x, 10.x.x.x

Solo funciona en tu red local

Uso: Dispositivos en tu casa/oficina

## IP Pública
Ejemplo: 8.8.8.8 (Google DNS)

Única en todo internet

Uso: Servidores web, APIs públicas

### 🏠 Analogía con direcciones postales:
IP Pública: "Calle Mayor 123, Madrid" - Te encuentra desde cualquier lugar

IP Privada: "Apartamento 2B" - Solo útil dentro del edificio

# 🚪 Puertos y Protocolos Esenciales para Desarrolladores Web

## 🔍 ¿Qué es un Puerto?
Un **puerto** es como un "número de puerta" virtual (0-65535) que permite a diferentes servicios comunicarse en una misma IP.  
📍 **Analogía**: Si una IP es una dirección de edificio, los puertos son los números de departamento.

## 🏆 Top 10 Puertos que Todo Dev Web Debe Conocer

| Puerto | Protocolo | Uso Típico                     | Comando Verificación       | Seguridad |
|--------|-----------|--------------------------------|---------------------------|-----------|
| **80** | HTTP      | Web no cifrada                 | `netstat -tuln \| grep 80` | ❌ Riesgo |
| **443**| HTTPS     | Web segura (SSL/TLS)           | `openssl s_client -connect host:443` | ✅ Seguro |
| **22** | SSH       | Conexión remota segura         | `ssh -v user@host -p 22`  | ✅ Seguro* |
| **3306**| MySQL    | Bases de datos relacionales    | `telnet localhost 3306`   | 🔐 Con auth |
| **5432**| PostgreSQL | DB relacional avanzada       | `lsof -i :5432`           | 🔐 Con auth |
| **27017**| MongoDB  | Bases de datos NoSQL          | `mongosh --port 27017`    | ⚠️ Por defecto sin auth |
| **6379**| Redis    | Cache/Base de datos clave-valor| `redis-cli -p 6379`       | ⚠️ Comúnmente expuesto |
| **8000**| Dev Server | Servidores locales (Django/Flask)| `curl localhost:8000`   | ❌ Solo local |
| **3000**| Node.js  | Aplicaciones React/Next.js     | `lsof -i :3000`           | ❌ Solo dev |
| **8080**| Proxy/Alt HTTP | Alternativa a HTTP       | `netcat -zv host 8080`    | ⚠️ Depende de config |

## 💻 Comandos Útiles
```bash
# Ver puertos en uso
ss -tulnp  # Linux (moderno)
netstat -tuln  # Linux/macOS (legacy)

# Probar conexión a puerto
telnet example.com 80
nc -zv example.com 443

# Escanear puertos locales (solo diagnóstico)
nmap -sT -p- localhost  # Requiere instalación
```
🔐 Buenas Prácticas
Nunca expongas puertos de DB (3306, 5432) directamente a Internet

Usa SSH tunneling para conexiones seguras:
ssh -L 3306:localhost:3306 user@remote-host

Cambia puertos predeterminados en producción (ej: MySQL a 33060)

Firewall obligatorio:
```bash

sudo ufw allow 443/tcp  # Ejemplo para HTTPS
sudo ufw deny 22  # Bloquear SSH si no se usa
```

# 🌐 Protocolos Clave del Día a Día Web

## 1. 🔗 HTTP/HTTPS
HTTP (HyperText Transfer Protocol) es el protocolo básico para navegar por internet. Permite que tu navegador solicite y reciba páginas web desde los servidores. HTTPS es la versión segura que cifra toda la comunicación, protegiendo tu información personal y contraseñas. Es por eso que ves el candado 🔒 en tu navegador cuando visitas sitios seguros como bancos o tiendas online.
## 2. 🏷️ DNS (Domain Name System)
Es como la "guía telefónica" de internet. Cuando escribes google.com en tu navegador, DNS traduce ese nombre fácil de recordar a la dirección IP numérica real del servidor (como 172.217.164.110). Sin DNS, tendrías que memorizar números complicados para cada sitio web que quieras visitar.
## 3. 🏠 DHCP (Dynamic Host Configuration Protocol)
Es el protocolo que automáticamente asigna direcciones IP a los dispositivos cuando se conectan a una red. Cuando tu teléfono se conecta al WiFi de casa, DHCP le da una dirección IP única, configura la puerta de enlace y los servidores DNS. Sin DHCP, tendrías que configurar manualmente estos valores en cada dispositivo.
## 4. 🚚 TCP vs UDP
TCP (Transmission Control Protocol) es como un servicio de paquetería confiable que garantiza que todos los datos lleguen completos y en orden. UDP (User Datagram Protocol) es como enviar postales: más rápido pero sin garantía de entrega.

# 📊 Ejemplos de uso:

## 🌐 Navegación web (TCP):

Necesitas que todas las partes de una página web lleguen correctamente
TCP verifica que el texto, imágenes y código se descarguen sin errores
Si algo se pierde, TCP lo reenvía automáticamente

## 🎮 Streaming y videojuegos (UDP):

En Netflix o YouTube, si se pierde un fotograma, es mejor continuar que detenerse
En videojuegos online, es preferible tener respuesta rápida aunque ocasionalmente se pierda algún dato
UDP prioriza la velocidad sobre la perfección

## 📹 Videoconferencias (UDP):

En Zoom o Teams, es mejor que la conversación fluya aunque se corte brevemente
La comunicación en tiempo real requiere velocidad más que precisión absoluta

[🔼 Volver al inicio](#-Puertos-y-Protocolos-Esenciales-para-Desarrolladores-Web)


# 🔗 ¿Qué pasa cuando navegas a una página?
Proceso básico de conexión en la web paso a paso:

### 1. Escribes la URL
Tecleas "https://github.com" en tu navegador

### 2. Resolución DNS
Tu navegador pregunta: "¿Cuál es la IP de github.com?"

Respuesta: "140.82.114.4"

### 3. Establecimiento de conexión TCP
Tu navegador se conecta a 140.82.114.4:443

Handshake de 3 pasos: SYN → SYN-ACK → ACK

### 4. Negociación SSL/TLS
Se establece la conexión cifrada (HTTPS)

Intercambio de certificados y claves

### 5. Petición HTTP
Se envía: "GET / HTTP/1.1"

Incluye headers como User-Agent, Accept, etc.

### 6. Respuesta del servidor
GitHub responde con HTML, CSS, JavaScript

Status: 200 OK, Content-Type: text/html

### 7. Renderizado
Tu navegador construye la página que ves

Puede hacer peticiones adicionales para imágenes, CSS, etc.
