---
id: abuse-report
title: "Reportar abuso y contenido ilegal - ¡Todo lo que necesitas saber!"
description: "Cómo reportar abuso y contenido ilegal a ZAP-Hosting - Documentación de ZAP-Hosting.com"
sidebar_label: Reportar Abuso
---

## Introducción

Internet permite generar valor. El abuso perjudica a los usuarios y a los servicios. Nuestro objetivo es detectar y detener incidentes rápidamente. Puedes reportar sospechas de abuso a nuestro Equipo de Abuso. Revisamos cada informe, preservamos pruebas, actuamos bajo la ley aplicable y nuestras políticas, y notificamos a las autoridades competentes cuando es necesario.

## Tipo de Abuso

¡Hola, mi nombre es! El abuso puede presentarse de diferentes maneras. Reporta cualquier caso que se ajuste o esté cerca de las siguientes categorías:

<details>
  <summary>Spam</summary>

Mensajes no solicitados o masivos enviados a través de nuestros sistemas o contenido alojado que activa filtros de spam. Las variantes incluyen spam de correo electrónico, spam de comentarios, spam de enlaces SEO y creación automática de cuentas. Proporciona mensajes de muestra, encabezados, IPs del remitente y patrones de envío.

</details>

<details>
  <summary>Ataques y DDoS</summary>

Tráfico hostil destinado a interrumpir servicios o sondear sistemas. Las formas comunes son inundaciones volumétricas L3 L4, inundaciones HTTP en la capa 7, amplificación, intentos de inicio de sesión por fuerza bruta y escaneos de puertos agresivos. Los indicadores incluyen picos en PPS o Mbps, tasas elevadas de 4xx 5xx y repetidos fallos de autenticación desde fuentes rotativas.

</details>

<details>
  <summary>Violaciones de derechos de autor y marcas registradas</summary>

Distribución no autorizada de obras protegidas o mal uso de marcas registradas. Las variantes incluyen espejos de piratería, descargas crackeadas, suplantación de marca y dominios engañosos. Proporciona la obra, el titular de los derechos, la ubicación exacta y el estado de autorización.

</details>

<details>
  <summary>Phishing</summary>

Contenido diseñado para recolectar credenciales o datos de pago imitando marcas de confianza. Las variantes incluyen portales de inicio de sesión falsos, estafas de facturas, señuelos de QR o archivos adjuntos y fatiga de MFA. Especifica la marca objetivo, los puntos de captura y cómo difiere la página del sitio legítimo.

</details>

<details>
  <summary>GDPR</summary>

Procesamiento no autorizado, exposición o filtración de datos personales. Los casos típicos incluyen índices abiertos, buckets mal configurados, scraping sin una base legal y registros públicos. Describe las categorías de datos, el alcance, los sujetos afectados y la causa de la exposición.

</details>

<details>
  <summary>CSAM/SAM</summary>

Cualquier material que represente explotación sexual de humanos. Tolerancia cero.

</details>

<details>
  <summary>Contenido ilegal</summary>

Contenido que viola la ley aplicable, como propaganda extremista, amenazas, discursos de odio, incitación a la violencia o difamación. Las variantes incluyen doxxing, amenazas explícitas y materiales prohibidos por jurisdicción. Proporciona la ubicación exacta y, si se conoce, la base legal involucrada.

</details>

<details>
  <summary>Otros</summary>

Abuso que no se ajusta a lo anterior pero que aún perjudica a los usuarios o sistemas. Ejemplos incluyen alojamiento de malware, botnet C2, fraude y criptominería no autorizada. Comparte hashes, URLs, patrones C2 y anomalías en el uso de recursos.

</details>

## Información requerida

Para asegurar un informe completo y accionable, por favor proporciona detalles exhaustivos que nos permitan identificar el recurso, verificar el incidente y tomar las medidas adecuadas, incluyendo lo siguiente:
- Ubicación. URL, IP, puerto, nombre de host, ruta de archivo, hash
- Marcas de tiempo en UTC en formato YYYY-MM-DDTHH:MM:SSZ
- Descripción. Qué pasó, cómo se detectó, impacto observado
- Evidencia. Capturas de pantalla, registros de texto, correo electrónico completo con encabezados como EML, PCAP corto, NetFlow, encabezados HTTP

## Archivos aceptados y provisión

Proporciona evidencia en formatos claros y de una manera en que podamos acceder a ella de manera confiable. Adjunta archivos más pequeños a tu correo electrónico o aloja archivos grandes externamente. Adjunta archivos pequeños a medianos directamente. Prefiere formatos abiertos y sin modificar. El texto sin formato es mejor que las capturas de pantalla de texto.

Para archivos grandes, comparte un enlace de descarga estable. Debería ser recuperable sin interacción o incluir credenciales claras. Indica la ventana de validez del enlace. Agrega sumas de comprobación para permitir la verificación de integridad.

Utiliza formatos estándar como TXT, PDF, PNG, JPG, PCAP o PCAPNG, EML, HAR, CSV y JSON. No incluyas contraseñas, claves privadas o datos personales completos a menos que sea estrictamente necesario.

Para la calidad, envía correos electrónicos como EML con encabezados completos, registros como texto sin formato, rastreos de red como capturas cortas y relevantes de PCAP o PCAPNG, y capturas de pantalla en resolución original.

Por seguridad, redacta cualquier secreto; si es necesario, coloca los archivos en un archivo protegido por contraseña y comparte la contraseña por separado. Para CSAM/SAM, no transmitas archivos, solo proporciona enlaces.

## Ponte en contacto con nosotros

Envía tu informe a `abuse@zap-hosting.com`. Es importante usar un asunto claro como `Informe de Abuso Phishing` o `Informe de Abuso DDoS`. Envía un correo electrónico por incidente. El siguiente ejemplo muestra una solicitud completa:

```
Para: abuse@zap-hosting.com
Asunto: Informe de Abuso Fuerza Bruta (SSH)

Ubicación:
- IP objetivo: XXX.XX.XXX.XX
- Servicio: SSH
- Puerto: 22
- Nombre de host: v12345.zap-hosting.com

Marcas de tiempo (UTC):
- Primera vez visto: 2025-08-23T09:12:04Z
- Última vez visto: 2025-08-23T10:03:31Z

Descripción:
Intentos repetidos de inicio de sesión SSH con nombres de usuario y IPs de origen rotativos. Detectado a través de anomalías en auth.log y tasa de conexión elevada. Autenticación por contraseña desactivada después de la detección. No se observó inicio de sesión exitoso.

Evidencia:
- Extracto de auth.log con múltiples entradas de "Contraseña fallida" y "Usuario inválido"
- Fragmento de registro de fail2ban mostrando prohibiciones y direcciones de origen
- PCAP de 60 segundos capturando intentos de TCP al puerto 22
- Recuentos agregados: 12,438 intentos desde 352 IPs de origen
- Principales fuentes con información ASN

Extracto de registro de muestra:
2025-08-23T09:55:17Z sshd[2173]: Contraseña fallida para el usuario admin no válido desde XXX.X.XXX.XX puerto XXXX ssh2
2025-08-23T09:55:18Z sshd[2173]: Contraseña fallida para root desde XXX.X.XX
```

## ¿Qué sucede después?

Nuestro Equipo de Abuso procesa tu informe lo más rápido posible y responde prontamente. Revisamos el incidente y lo priorizamos por severidad.

Basándonos en la revisión, tomamos acciones que incluyen notificación al cliente, suspensión temporal/permanente, eliminación del contenido reportado, preservación de pruebas y notificación a las autoridades competentes cuando sea necesario.