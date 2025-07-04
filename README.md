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

El Modelo TCP/IP: Las 4 Capas Fundamentales

El modelo TCP/IP es la base de internet y define cómo los datos viajan a través de la red. Está compuesto por cuatro capas que trabajan en conjunto:

1. Capa de Aplicación
Esta es la capa más cercana al usuario final. Aquí residen los programas y servicios que utilizamos diariamente como navegadores web, correo electrónico, transferencia de archivos y mensajería. Los protocolos más comunes incluyen HTTP/HTTPS para páginas web, SMTP para correo electrónico, y FTP para transferencia de archivos. Esta capa se encarga de presentar la información de manera que las aplicaciones puedan procesarla.

2. Capa de Transporte
Actúa como el intermediario confiable entre las aplicaciones y la red. Su función principal es asegurar que los datos lleguen completos y en el orden correcto. Utiliza principalmente dos protocolos: TCP (Transmission Control Protocol) que garantiza la entrega confiable de datos, y UDP (User Datagram Protocol) que es más rápido pero no garantiza la entrega. Esta capa también maneja la división de datos en segmentos y su posterior recomposición.

3. Capa de Internet
Es el cerebro del enrutamiento en la red. Su responsabilidad es encontrar la mejor ruta para que los datos viajen desde el origen hasta el destino, sin importar cuántos dispositivos intermedios (routers) deban atravesar. El protocolo IP (Internet Protocol) es el protagonista aquí, asignando direcciones únicas a cada dispositivo y determinando cómo los paquetes de datos navegan por la red global.

4. Capa de Acceso a Red
Representa la conexión física y lógica directa entre dispositivos. Incluye tanto el hardware (cables, tarjetas de red, antenas WiFi) como los protocolos que controlan cómo los datos se transmiten físicamente. Esta capa maneja tecnologías como Ethernet para redes cableadas, WiFi para conexiones inalámbricas, y otros métodos de acceso al medio físico de transmisión.

Cada capa depende de las demás: cuando envías un mensaje, comienza en la capa de aplicación y desciende hasta la capa de acceso a red para ser transmitido. Al llegar al destino, el proceso se invierte, subiendo capa por capa hasta llegar a la aplicación receptora.

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

[🔼 Volver al inicio](#-Puertos-y-Protocolos-Esenciales-para-Desarrolladores-Web)