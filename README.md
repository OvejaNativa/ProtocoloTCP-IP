# �� Conceptos Básicos del Protocolo TCP/IP

Este documento forma parte del módulo introductorio de redes en el bootcamp de desarrollo web. Estos son los fundamentos esenciales del protocolo TCP/IP, necesario para entender cómo viajan los datos por Internet y cómo funcionan los servicios web.

---

## �� Tabla de Contenidos

1. **�� ¿Qué es el protocolo TCP/IP y por qué es importante?**

   - Breve historia y propósito: 
   - Su rol en el funcionamiento de Internet

Actualmente la mayoría de ordenadores están conectados a alguna red (internet, intranet, etc.) y casi todos lo hacen utilizando el modelo TCP/IP. Este modelo es un protocolo para comunicación en redes que permite que un equipo pueda comunicarse dentro de una red. El protocolo TCP/IP surgió de un proyecto de defensa llamado DARPA en 1969. En 1983 el nuevo conjunto de protocolos TCP/IP fue adoptado como estándar y finalmente se convirtió en el más usado en redes y el protocolo estándar de internet. El modelo TCP/IP permite un intercambio de datos fiable dentro de una red, definiendo los pasos a seguir desde que se envían los datos (en paquetes) hasta que son recibidos. Para lograrlo utiliza un sistema de capas con jerarquías (se construye una capa a continuación de la anterior) que se comunican únicamente con su capa superior (a la que envía resultados) y su capa inferior (a la que solicita servicios).



2. **��️ Modelo TCP/IP vs Modelo OSI** (CATA)

   - Comparación de capas 
Modelo OSI (Open System Interconnection) tiene 7 capas, mientras que Modelo TCP/IP tiene 4 (aplicación, transporte, acceso a red, internet). TCP/IP es el que usamos.
   - ¿Por qué usamos TCP/IP en la web?
TCP/IP se enfoca en la transmisión de datos de forma eficiente. Su uso en web es debido a ser más práctico, a su vez bien adaptado a servicios de red modernos.

3. **�� Las 4 capas del modelo TCP/IP (de forma sencilla)**

   - Capa de Aplicación (HTTP, HTTPS, DNS, etc.)
   - Capa de Transporte (TCP vs UDP)
   - Capa de Internet (IP, direcciones IP, routing)
   - Capa de Acceso a Red (Ethernet, Wi-Fi)
   El modelo TCP/IP (también conocido como el modelo de Internet) está compuesto por 4 capas, cada una con funciones específicas en la transmisión de datos a través de redes. Estas capas son:
1. Capa de Aplicación

    Función: Proporciona servicios de red directamente a las aplicaciones del usuario.

    Protocolos comunes: HTTP, FTP, SMTP, DNS, POP3, IMAP.
•	HTTP significa Hypertext Transfer Protocol (Protocolo de Transferencia de Hipertexto). Es un protocolo de nivel de aplicación que permite la comunicación entre clientes (normalmente navegadores web) y servidores web. Se utiliza principalmente para transmitir páginas web (HTML), imágenes, scripts y otros recursos.
	
•	FTP significa File Transfer Protocol (Protocolo de Transferencia de Archivos). Es un protocolo de la capa de aplicación diseñado para transferir archivos entre un cliente y un servidor a través de una red.
	Funciones principales de FTP
1.	Subir archivos del cliente al servidor
2.	Descargar archivos del servidor al cliente
3.	Crear, renombrar, mover o borrar archivos y carpetas en el servidor
4.	Autenticación de usuario mediante nombre de usuario y contraseña

•	HTTPS significa Hypertext Transfer Protocol Secure (Protocolo Seguro de Transferencia de Hipertexto). Es la versión segura de HTTP. Se utiliza principalmente para navegar de forma segura por la web.

•	DNS significa Domain Name System (Sistema de Nombres de Dominio). Es un servicio de la capa de aplicación que traduce nombres de dominio (ej. www.google.com) en direcciones IP (ej. 142.250.190.4) que las computadoras pueden entender.
Equivalente en OSI: Capas 5 (Sesión), 6 (Presentación) y 7 (Aplicación).

2. Capa de Transporte
    Función: Asegura la comunicación confiable entre dispositivos, control de flujo y corrección de errores.
    Protocolos comunes:
•	TCP (Transmission Control Protocol): Confiable, orientado a conexión.
•	UDP (User Datagram Protocol): No confiable, sin conexión.
Característica	TCP	UDP
Tipo de conexión	Orientado a conexión	No orientado a conexión
Fiabilidad	Confiable (garantiza entrega y orden)	No confiable
Control de flujo	Sí	No
Control de congestión	Sí	No
Velocidad	Más lento	Más rápido
Tamaño de cabecera	Más grande (20 bytes mínimo)	Más pequeña (8 bytes)
Usos principales	Web, email, FTP	Streaming, juegos, DNS, VoIP

    Equivalente en OSI: Capa 4 (Transporte).

3. Capa de Internet
    Función: Encargada del direccionamiento lógico, enrutamiento de paquetes y su entrega.
Protocolos comunes: IP (IPv4/IPv6), ICMP, ARP.
•	IP significa Internet Protocol (Protocolo de Internet).
Es el protocolo principal de la Capa de Internet.
Su función es encaminar los paquetes (datagramas) desde el origen hasta el destino a través de una o varias redes.
Versiones principales
🔸 IPv4:
1.	Más usado actualmente.
2.	Direcciones de 32 bits (4 bytes), ej.: 192.0.2.1
3.	Tiene limitación de direcciones (unos 4 mil millones).
🔸 IPv6:
1.	Diseñado para reemplazar IPv4.
2.	Direcciones de 128 bits, ej.: 2001:0db8::1
3.	Prácticamente direcciones ilimitadas.

•	
  Equivalente en OSI: Capa 3 (Red).

4. Capa de Acceso a la Red (o de Enlace)
 Función: Define cómo se transmiten los datos a través del hardware de red (como cables, switches, NICs).
Protocolos comunes: Ethernet, Wi-Fi, PPP, ARP (también puede estar aquí).
Ethernet es una tecnología de red de área local (LAN).
Es uno de los protocolos más usados en la Capa de Acceso a Red (también llamada Capa de Enlace).
Define cómo se transmiten los datos a través del medio físico (cable UTP, fibra óptica, etc.).
Wi-Fi es una tecnología de red inalámbrica basada en el estándar IEEE 802.11.
Permite la transmisión de datos por ondas de radio, eliminando la necesidad de cables físicos.
Equivalente en OSI: Capas 1 (Física) y 2 (Enlace de datos).

4. **�� Direccionamiento IP: IPv4 vs IPv6**

   - Qué es una dirección IP
R// 🌐 ¿Qué es una dirección IP?
Una dirección IP (Internet Protocol) es un identificador único asignado a cada dispositivo conectado a una red que utiliza el protocolo de internet. Es como la dirección postal digital que permite que los datos lleguen al destino correcto.

   - Estructura básica de una IP
R// 🧱 IPv4 – Estructura clásica
Formato: A.B.C.D (cuatro números separados por puntos)
Cada número va de: 0 a 255
Ejemplo: 192.168.1.100
Tamaño: 32 bits
Total de direcciones posibles: Unos 4.3 mil millones
🔹 Ejemplo explicado: 192.168.1.100 →
192, 168, 1, y 100 representan octetos de 8 bits
Cada octeto se transforma en binario para ser interpretado por las máquinas
🚀 IPv6 – La nueva generación
Formato: Ocho bloques de 4 dígitos hexadecimales separados por :
Ejemplo: 2001:0db8:85a3:0000:0000:8a2e:0370:7334
Tamaño: 128 bits
Capacidad: ¡Más de 340 sextillones de direcciones!
🔹 Atajo útil: Si hay grupos de ceros consecutivos, se pueden abreviar usando :: Ejemplo corto: 2001:db8:85a3::8a2e:370:7334
🎯 En resumen
Elemento
IPv4
IPv6
Longitud
32 bits
128 bits
Separación
Puntos (.)
Dos puntos (:)
Base numérica
Decimal (0–255)
Hexadecimal (0–FFFF)
Ejemplo
192.168.1.1
fe80::1ff:fe23:4567:890a


   - Diferencia entre IP pública y privada
🔐 Diferencia entre IP pública y privada
Tipo
Visible desde internet
Usada para...
Ejemplo
Pública
✅ Sí
Identificar tu red ante el mundo
181.45.123.10
Privada
❌ No
Comunicación interna dentro de redes locales (LAN)
192.168.1.1, 10.0.0.1

IP pública: Asignada por tu proveedor de internet. Es tu “cara” en internet.
IP privada: Usada para identificar dispositivos dentro de una misma red local (como tu router, tu teléfono, etc.)



5. **�� Puertos y Protocolos Comunes para Desarrolladores Web**

   - ¿Qué es un puerto? En informática, un puerto es una interfaz a través de la cual se pueden enviar y recibir los diferentes tipos de datos. En electrónica, telecomunicaciones y hardware, una interfaz es el puerto (circuito físico) a través del que se envían o reciben señales desde un sistema o subsistemas hacia otros.

   - Puertos típicos: 80 (HTTP), 443 (HTTPS), 22 (SSH), 3306 (MySQL)
Puerto 80: Web (HTTP)
Puerto 443: Web segura (HTTPS)
Puerto 43: Sistema de nombres de dominio (DNS)
Puerto 3389: Protocolo de escritorio remoto (RDP)
Puerto 21: Protocolo de transferencia de archivos (FTP)
Puerto 22: Comunicaciones seguras (SSH), un protocolo de túnel utilizado para crear conexiones de red seguras
Puero 3306: MySQL usa este puerto por defecto


6. **��️ Protocolos clave en el día a día web** (CATA)

   - HTTP/HTTPS: Usado para navegar sitios web. HTTPS: versión segura.
   - DNS: Traduce nombres a direcciones IP.
   - DHCP: Asigna direcciones IP a dispositivos de una red.
   - TCP vs UDP (con ejemplos como streaming vs navegación): TCP usado para navegación web y correos; UDP usado para streaming y videojuegos (prioriza velocidad).

7. **�� Proceso básico de conexión en la web**

   - De tu navegador a un servidor web: ¿qué ocurre paso a paso?
   - Resolución DNS
   - Establecimiento de conexión TCP (Handshake)
   1.	Escribir la URL
      El usuario escribe la dirección en el navegador
   2.	Resolución DNS
   El navegador necesita saber la dirección IP de www.ejemplo.com.
   •	Busca en su caché local o en el sistema operativo si ya conoce la IP.
   •  Si no la tiene, hace una consulta DNS (usando UDP puerto 53) a un servidor DNS.
   •	El servidor DNS responde


8. **�� Seguridad y capa de transporte**

   - Introducción rápida a SSL/TLS
La capa de transporte, ubicada en el modelo OSI, garantiza la entrega confiable de datos entre dispositivos. Cuando hablamos de seguridad en esta capa, entran en juego protocolos como:
SSL (Secure Sockets Layer): fue el primer intento ampliamente adoptado de cifrado en la web, hoy obsoleto.
TLS (Transport Layer Security): sucesor de SSL, más robusto y seguro. Aunque muchos aún dicen "certificado SSL", lo que se usa hoy es TLS.
💡 TLS cifra los datos que se envían por la red, evitando que sean interceptados o alterados.















   - Qué cambia cuando usamos HTTPS
🌐 ¿Qué cambia cuando usamos HTTPS?
Pasar de HTTP a HTTPS implica una transformación radical en términos de seguridad y confianza del usuario:
Característica
HTTP
HTTPS (con TLS)
🔒 Seguridad
Ninguna (datos visibles)
Cifrado de extremo a extremo
🌍 Dirección web
http://
https://
🔐 Certificado digital
No requerido
Sí, obligatorio
🧠 Integridad de datos
Riesgo de manipulación
Verificación asegurada
👁️ Protección de privacidad
No
Sí, oculta datos sensibles
🔎 Icono del navegador
Sin candado
Candado visible (¡confianza para usuarios!)


📌 Ejemplo en la vida real: Si un usuario ingresa su información médica o datos de su mascota en Health Mood, HTTPS con TLS asegura que esa información no pueda ser interceptada o modificada en el camino entre su navegador y tu servidor 🐾. 




















9. **�� Herramientas básicas para ver el protocolo en acción**

   - `ping`, `tracert`/`traceroute`
   - `netstat`, `nslookup`, `curl`, `telnet`


🛠️ Herramientas de Diagnóstico de Red
Herramienta
Función Principal
Comando de Ejemplo
¿Para qué sirve?
ping
Verifica la conectividad y mide latencia
ping google.com
Ver si hay conexión y cuánto demora en responder
tracert / traceroute
Muestra la ruta que siguen los paquetes
tracert healthmood.cl / traceroute healthmood.cl
Identificar dónde puede estar fallando la conexión
netstat
Muestra conexiones activas y puertos en uso
netstat -an
Detectar servicios en uso o conexiones sospechosas
nslookup
Consulta DNS para traducir nombres en IP
nslookup healthmood.cl
Diagnosticar problemas con la resolución de nombres
curl
Envía solicitudes HTTP(S) y muestra la respuesta
curl -I https://healthmood.cl
Ver cabeceras, estado de HTTPS o probar APIs
telnet
Prueba conectividad con un puerto específico
telnet healthmood.cl 443
Ver si un servicio está activo y escucha correctamente













10. **�� Glosario esencial de términos**

- IP, DNS, Gateway, NAT, Subred, Paquete, etc.
📘 Glosario Esencial de Redes
Término
Definición breve
IP (Internet Protocol)
Dirección única que identifica un dispositivo en una red (como una dirección postal digital).
DNS (Domain Name System)
Sistema que traduce nombres de dominio (healthmood.cl) en direcciones IP numéricas.
Gateway
Dispositivo (como un router) que conecta redes distintas, funcionando como un puente entre una red local e internet.
NAT (Network Address Translation)
Técnica que permite que múltiples dispositivos usen una misma IP pública para salir a internet, traduciendo direcciones privadas a públicas.
Subred (Subnet)
Segmento lógico de una red mayor que permite organizar y optimizar el tráfico interno.
Paquete
Unidad de datos que viaja por la red. Contiene la información y metadatos necesarios para su entrega.
MAC (Media Access Control)
Dirección física única que identifica una tarjeta de red (nivel hardware).
Puertos
Puntos lógicos en un dispositivo que permiten distinguir distintos servicios de red (por ejemplo, puerto 80 para HTTP).
Protocolo
Conjunto de reglas para la comunicación entre dispositivos (ej: TCP/IP, HTTP, HTTPS).
LAN (Local Area Network)
Red local que conecta dispositivos en un espacio reducido (como una oficina o casa).
WAN (Wide Area Network)
Red de gran escala como internet, que conecta múltiples redes


