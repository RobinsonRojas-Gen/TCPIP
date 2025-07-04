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

# 🛠️ Herramientas Esenciales para Analizar Redes y Protocolos

## 📌 Comandos Básicos de Diagnóstico

| Herramienta  | Plataforma | Uso Principal | Comando Ejemplo | Visualización |
|--------------|-----------|---------------|-----------------|---------------|
| **`ping`** 🏓 | Multiplataforma | Verificar conectividad básica | `ping google.com` | ⏱️ Tiempo de respuesta |
| **`tracert`/`traceroute`** 🗺️ | Windows/Linux | Rastrear ruta de paquetes | `tracert google.com` (Win)<br>`traceroute -I google.com` (Linux) | 🌍 Saltos de red |
| **`netstat`** 📊 | Multiplataforma | Mostrar conexiones activas | `netstat -tuln` (Linux/macOS)<br>`netstat -ano` (Windows) | 🔗 Puertos abiertos |
| **`nslookup`** 🔍 | Multiplataforma | Consultar registros DNS | `nslookup google.com`<br>`nslookup -type=mx google.com` | 📝 Registros DNS |
| **`curl`** 🌐 | Multiplataforma | Transferencia de datos HTTP | `curl -v https://google.com`<br>`curl -I https://google.com` | 📦 Headers/Contenido |
| **`telnet`** 🔌 | Multiplataforma | Probar conectividad a puertos | `telnet google.com 80` | ✉️ Comunicación raw |

## 🎯 Casos de Uso Prácticos

### 1. Diagnóstico de Conexión Básica
```bash

/macOS/Windows)
ping -c 4 google.com  # Linux/macOS
ping -n 4 google.com  # Windows
```
Salida típica:
```bash

64 bytes from 172.217.0.46: icmp_seq=0 ttl=115 time=25.3 ms
```

2. Analizar Ruta de Red
```bash

# Windows
tracert google.com

# Linux (requiere instalación)
sudo apt install traceroute
traceroute -I google.com  # Usa ICMP
```
3. Inspeccionar Conexiones Activas
```bash

# Linux/macOS (puertos escuchando)
netstat -tuln | grep LISTEN

# Windows (con PID)
netstat -ano | findstr LISTENING
```
4. Depuración HTTP/API con Curl
```bash

# Ver headers completos (útil para APIs)
curl -v https://api.example.com/users

# Solo headers de respuesta
curl -I https://google.com

# Enviar JSON (POST request)
curl -X POST -H "Content-Type: application/json" -d '{"user":"test"}' https://api.example.com/login
```
# 🛠️ Herramientas Básicas para Ver TCP/IP en Acción

Estas herramientas te permiten explorar y diagnosticar cómo funciona el protocolo TCP/IP en tiempo real:

## 🏓 ping
Verificar si un dispositivo está vivo
Envía pequeños paquetes de datos a una dirección IP para verificar si está disponible y medir el tiempo de respuesta.
bashping google.com
ping 8.8.8.8
¿Qué hace? 📡 Envía paquetes ICMP y espera respuesta
Útil para: Verificar conectividad, medir latencia, diagnosticar problemas de red

## 🗺️ tracert/traceroute
Seguir la ruta de tus datos
Muestra todos los routers intermedios por los que pasan tus datos hasta llegar al destino.
bash# Windows
tracert google.com

## Linux/Mac
traceroute google.com
¿Qué hace? 🛤️ Rastrea cada salto en la ruta de red
Útil para: Identificar dónde se pierde la conexión, ver la geografía de internet

## 📊 netstat
Ver conexiones activas
Muestra todas las conexiones de red activas en tu dispositivo y qué programas las están usando.
bashnetstat -an    # Mostrar todas las conexiones
netstat -b     # Mostrar qué programa usa cada conexión
¿Qué hace? 🔍 Lista puertos abiertos y conexiones establecidas
Útil para: Detectar programas que usan internet, verificar servicios activos

## 🔍 nslookup
Consultar el DNS
Traduce nombres de sitios web a direcciones IP y viceversa, como un directorio telefónico de internet.
bashnslookup google.com
nslookup 8.8.8.8
¿Qué hace? 📞 Consulta servidores DNS para resolver nombres
Útil para: Verificar si un dominio existe, encontrar la IP de un sitio web

## 🌐 curl
Descargar contenido web
Obtiene páginas web, archivos o datos de servidores directamente desde la línea de comandos.
bashcurl https://google.com
curl -I https://github.com    # Solo headers
curl -o archivo.zip https://ejemplo.com/archivo.zip
¿Qué hace? 📥 Realiza peticiones HTTP/HTTPS y muestra la respuesta
Útil para: Probar APIs, descargar archivos, verificar respuestas de servidores

## 📞 telnet
Conexión directa a servicios
Establece una conexión de texto plano con cualquier servicio de red para comunicarse directamente.
bashtelnet google.com 80
telnet smtp.gmail.com 25
¿Qué hace? 🔗 Conecta directamente a puertos específicos
Útil para: Probar si un servicio está funcionando, enviar comandos manuales

## 🎯 Ejemplo Práctico
Para diagnosticar problemas de conexión a github.com:

ping github.com 🏓 → ¿Está disponible?
traceroute github.com 🗺️ → ¿Por dónde viajan mis datos?
nslookup github.com 🔍 → ¿Qué IP tiene?
curl -I https://github.com 🌐 → ¿Responde el servidor web?
telnet github.com 443 📞 → ¿Está abierto el puerto HTTPS?

¡Así puedes ver TCP/IP trabajando en tiempo real! ⚡

---

# 📚 Glosario de Términos Esenciales
**IP (Internet Protocol)**
Dirección única que identifica un dispositivo en la red

**DNS (Domain Name System)**
Sistema que convierte nombres de dominio en direcciones IP

**Gateway**
Punto de acceso entre dos redes diferentes (tu router)

**NAT (Network Address Translation)**
Permite que múltiples dispositivos compartan una IP pública

**Subred**
División lógica de una red IP (ej: 192.168.1.0/24)

**Paquete**
Unidad básica de datos que viaja por la red

**Socket**
Combinación de IP + Puerto (ej: 192.168.1.1:3000)

**Firewall**
Sistema que controla el tráfico de red entrante y saliente

**Proxy**
Intermediario que actúa en nombre de otros dispositivos

**Load Balancer**
Distribuye el tráfico entre múltiples servidores

**CDN (Content Delivery Network)**
Red de servidores distribuidos para acelerar la entrega de contenido

**Handshake**
Proceso de establecimiento de conexión entre cliente y servidor

**Bandwidth**
Cantidad máxima de datos que puede transmitir una conexión

**Latency**
Tiempo que tarda un paquete en viajar del origen al destino

**🎯 Resumen para Desarrolladores Web**
Los conceptos más importantes que debes recordar:

**HTTP/HTTPS:** Siempre usa HTTPS en producción
**DNS:** Entender cómo se resuelven los dominios
**Puertos:** Conocer los puertos comunes (80, 443, 22, 3000)
**TCP vs UDP:** TCP para datos críticos, UDP para velocidad
**IP privada vs pública:** Fundamental para configurar servidores
**Herramientas:** DevTools, curl, ping para debugging

---
