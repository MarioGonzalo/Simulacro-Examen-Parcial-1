**Repositorio:** https://github.com/MarioGonzalo/Simulacro-Examen-Parcial-1.git <br> 
**Pages:** https://mariogonzalo.github.io/Simulacro-Examen-Parcial-1/

# Simulacro-Examen-Parcial-1

# Pregunta 1: Modelos OSI y TCP/IP

## Diferencias entre el modelo OSI y el modelo TCP/IP

| **Criterio**        | **Modelo OSI** | **Modelo TCP/IP** |
|---------------------|---------------|-------------------|
| **Número de capas** | 7 capas (Física, Enlace de datos, Red, Transporte, Sesión, Presentación, Aplicación). | 4 capas (Acceso a la red, Internet, Transporte, Aplicación). |
| **Orientación**     | Modelo teórico desarrollado por la ISO para estandarizar la comunicación en redes. | Modelo práctico basado en la implementación real de protocolos en Internet. |
| **Capa de aplicación** | Separa las funciones en tres capas: Aplicación, Presentación y Sesión. | Une estas funciones en la capa Aplicación. |
| **Flexibilidad**    | Es más estructurado y modular, facilita la enseñanza y comprensión conceptual. | Es más simplificado y eficiente para la implementación práctica. |

## Ventajas y limitaciones de los modelos

| **Modelo**   | **Ventajas** | **Limitaciones** |
|-------------|-------------|-----------------|
| **OSI**     | - Claramente definido y estructurado.<br>- Facilita la comprensión del funcionamiento de redes.<br>- Permite la operar entre diferentes tecnologías. | - No se implementa directamente en la mayoría de las redes.<br>- Puede ser más complejo en comparación con el modelo TCP/IP. |
| **TCP/IP**  | - Basado en estándares ampliamente utilizados en redes reales (como Internet).<br>- Más eficiente y práctico.<br>- Fácilmente escalable y adaptable. | - No separa claramente algunas funciones como en OSI.<br>- No define explícitamente capas de sesión y presentación.<br>- No es ideal para describir todos los tipos de redes. |

# Pregunta 2: Función de la Capa de Transporte

## En el Modelo OSI:
- Es la cuarta capa del modelo OSI.
- Proporciona un servicio fiable o no fiable para la comunicación entre procesos en dispositivos finales.
- Se encarga de:
  - Segmentación y reensamblado de datos.
  - Control de flujo para evitar saturación del receptor.
  - Corrección de errores para garantizar la entrega correcta.
- Puede operar en dos modos:
  - **Orientado a conexión**: Asegura la entrega ordenada de datos.
  - **No orientado a conexión**: Envío rápido sin verificación de entrega.
- **Ejemplo**:  
  - Al descargar un archivo desde un servidor web, se usa TCP para garantizar que el archivo llegue sin errores ni pérdida de datos.

## En el Modelo TCP/IP:
- Es la tercera capa del modelo TCP/IP.
- Garantiza que los datos sean transmitidos de manera eficiente entre aplicaciones.
- Implementa:
  - Multiplexación de datos para que varias aplicaciones usen la red simultáneamente.
  - Gestión de sesiones mediante puertos (ejemplo: el puerto 80 para HTTP).
  - Encapsulación de datos para que sean transportados en la red correctamente.
- **Ejemplo**:  
  - Al hacer una videollamada, se usa UDP, ya que la prioridad es la velocidad en tiempo real, aunque algunos paquetes se pierdan.

## Garantía de Entrega de Datos:
- **TCP (Transmission Control Protocol)**:
  - Garantiza que los datos lleguen completos y en orden.
  - Utiliza un mecanismo de confirmación (ACK) para verificar la recepción de los paquetes.
  - Implementa control de congestión y retransmisión de paquetes perdidos.
  - **Ejemplo**:
    - Al enviar un correo electrónico con SMTP, TCP garantiza que el mensaje llegue sin errores.
- **UDP (User Datagram Protocol)**:
  - No garantiza la entrega ni el orden de los paquetes, pero es más rápido.
  - Se usa en aplicaciones donde la velocidad es más importante que la precisión.
  - **Ejemplo**:
    - En un videojuego en línea, UDP permite enviar información de posición y movimientos con mínima latencia, aunque se pierdan algunos paquetes.
   
# Pregunta 3: TCP vs. UDP

## 1. Orientación a Conexión
- **TCP (Transmission Control Protocol)**:
  - **Orientado a conexión**: Antes de enviar datos, establece una conexión mediante el handshake de tres vías (SYN, SYN-ACK, ACK).
  - Asegura que haya un canal de comunicación estable entre el emisor y el receptor antes de la transmisión.
- **UDP (User Datagram Protocol)**:
  - **No orientado a conexión**: No requiere establecer una conexión previa.
  - Los datos se envían sin verificar si el destinatario los recibe.

## 2. Fiabilidad y Control de Errores
- **TCP**:
  - **Fiable**: Garantiza la entrega de los datos sin errores, sin duplicaciones y en el orden correcto.
  - Usa mecanismos como:
    - **Acuses de recibo (ACKs)**.
    - **Reenvío de paquetes perdidos**.
    - **Corrección de errores y control de flujo**.
- **UDP**:
  - **No fiable**: No verifica si los paquetes llegan ni si lo hacen en orden.
  - No ofrece retransmisión ni corrección de errores, lo que puede provocar pérdida de datos.

## 3. Velocidad y Orden de Entrega
- **TCP**:
  - Más lento debido a sus procesos de control de errores, retransmisión y control de congestión.
  - Mantiene el orden de entrega de los paquetes.
- **UDP**:
  - Más rápido, ya que no tiene control de errores ni confirmaciones de recepción.
  - No garantiza el orden de entrega de los paquetes.

## 4. Ejemplos de Aplicaciones
- **TCP**:
  - Se usa cuando la fiabilidad es prioritaria sobre la velocidad.
  - **Ejemplos**:
    - **Navegación web (HTTP/HTTPS)** → Las páginas deben cargarse completamente.
    - **Transferencia de archivos (FTP, SFTP)** → Los datos deben llegar íntegros.
    - **Correo electrónico (SMTP, IMAP, POP3)** → Mensajes completos y sin errores.
    - **Mensajería instantánea (WhatsApp, Telegram - mensajes de texto)** → Asegura que cada mensaje llegue correctamente.
- **UDP**:
  - Se usa cuando la velocidad es más importante que la precisión.
  - **Ejemplos**:
    - **Streaming de video y audio (YouTube, Netflix, Spotify, Twitch, VoIP)** → Un pequeño retraso o pérdida de paquetes no afecta mucho la experiencia.
    - **Videojuegos en línea** → Se prioriza la latencia baja sobre la fiabilidad.
    - **Llamadas y videoconferencias (Zoom, Microsoft Teams, Skype)** → Prefiere velocidad a retransmisión de datos perdidos.
    - **Sistemas de radiodifusión** → Envía datos a múltiples usuarios sin necesidad de confirmación.



