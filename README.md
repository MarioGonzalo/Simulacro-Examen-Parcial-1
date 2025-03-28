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

