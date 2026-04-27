## 💻 Entorno de Pruebas (Lab Environment)
Para garantizar la seguridad y el aislamiento, las auditorías se realizan en un entorno controlado:
- **Hardware:** HP 630 dedicado exclusivamente a testing.
- **Configuración:** Dual Boot mediante particionamiento de disco.
- **Sistemas:** - **Ubuntu Linux:** Utilizado para herramientas de auditoría (Nmap, Wireshark).
  - **Windows 11:** Utilizado para análisis de comportamiento y comparativa de red.
 
  - # 🌐 Auditoría de Red y Análisis de Tráfico (Reconocimiento Activo/Pasivo)

## 📝 Descripción Detallada
Este proyecto documenta un ejercicio de reconocimiento y análisis de seguridad sobre un entorno web real (Gemma Estilistas). El objetivo fue identificar la infraestructura del servidor, los servicios expuestos y validar el uso de herramientas de anonimización durante procesos de auditoría técnica.

## 🛠️ Metodología y Hallazgos Técnicos

### 1. Análisis de Tráfico y Resolución DNS (Wireshark)
Utilizando **Wireshark** en la interfaz de red activa, se capturó el tráfico generado al consultar el dominio. 
- **Protocolo:** Se analizó el protocolo **DNS** (Domain Name System).
- **Hallazgo:** Localización de la dirección IP real del servidor mediante el filtrado de paquetes de **respuesta DNS**, identificando el destino final antes de iniciar el escaneo activo.

### 2. Escaneo de Puertos y Superficie de Ataque (Nmap)
Una vez obtenida la IP, se procedió a un escaneo de puertos para determinar los servicios activos:
- **Puertos Abiertos:** - **80/tcp (HTTP):** Servicio web estándar.
    - **443/tcp (HTTPS):** Servicio web cifrado mediante TLS.
- **Puertos Cerrados:** - **21 (FTP) y 22 (SSH):** Se confirmó que estos vectores comunes de intrusión están debidamente cerrados/protegidos.

### 3. Ofuscación de Identidad y Protocolos Modernos (Proton VPN)
Para mitigar el riesgo de exposición de la IP pública personal durante la fase de reconocimiento, se implementó **Proton VPN**.
- **Observación Técnica:** Se verificó que el túnel de la VPN generó una dirección **IPv6**, demostrando la compatibilidad del entorno de laboratorio con los protocolos de red de nueva generación.

## 🛡️ Competencias Demostradas
- Gestión de particionamiento de sistemas operativos (Linux/Windows). 
- Análisis forense de red y decodificación de protocolos. 
- Uso profesional de herramientas CLI (Línea de comandos) y GUI de seguridad.
