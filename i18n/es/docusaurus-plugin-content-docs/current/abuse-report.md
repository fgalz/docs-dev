---
id: abuse-report
title: "¡Reporta abuso y contenido ilegal - Todo lo que necesitas saber!"
description: "Cómo reportar abuso y contenido ilegal a ZAP-Hosting - Documentación de ZAP-Hosting.com"
sidebar_label: Reportar Abuso
---

## Introducción

Internet habilita el valor. El abuso perjudica a los usuarios y servicios. Nuestro objetivo es detectar y detener incidentes rápidamente. Puedes reportar sospechas de abuso a nuestro Equipo de Abuso. Revisamos cada reporte, preservamos evidencia, actuamos conforme a la ley aplicable y nuestras políticas, y notificamos a las autoridades competentes cuando es necesario.

## Tipos de Abuso

El abuso puede presentarse de diferentes maneras. Reporta cualquier caso que encaje o se acerque a las siguientes categorías:

<details>
  <summary>Spam</summary>

Mensajes no solicitados o masivos enviados a través de nuestros sistemas o contenido alojado que activa filtros de spam. Las variantes incluyen spam por correo electrónico, spam en comentarios, spam de enlaces SEO y creación automatizada de cuentas. Proporciona ejemplos de mensajes, encabezados, IPs de remitente y patrones de envío.

</details>

<details>
  <summary>Ataques y DDoS</summary>

Tráfico hostil destinado a interrumpir servicios o explorar sistemas. Las formas comunes son inundaciones volumétricas L3 L4, inundaciones HTTP capa-7, amplificación, intentos de inicio de sesión por fuerza bruta y escaneos de puertos agresivos. Los indicadores incluyen picos en PPS o Mbps, tasas elevadas de errores 4xx 5xx y fallos de autenticación repetidos desde fuentes rotativas.

</details>

<details>
  <summary>Violaciones de derechos de autor y marcas registradas</summary>

Distribución no autorizada de obras protegidas o uso indebido de marcas registradas. Las variantes incluyen espejos de piratería, descargas crackeadas, suplantación de marca y dominios engañosos. Proporciona la obra, titular de los derechos, ubicación exacta y estado de autorización.

</details>

<details>
  <summary>Phishing</summary>

Contenido diseñado para recolectar credenciales o datos de pago imitando marcas de confianza. Las variantes incluyen portales de inicio de sesión falsos, estafas de facturas, cebos con QR o archivos adjuntos y fatiga de MFA. Especifica la marca objetivo, puntos de captura y cómo la página difiere del sitio legítimo.

</details>

<details>
  <summary>GDPR</summary>

Procesamiento, exposición o filtración no autorizada de datos personales. Los casos típicos incluyen índices abiertos, buckets mal configurados, scraping sin base legal y registros públicos. Describe las categorías de datos, alcance, sujetos afectados y la causa de la exposición.

</details>

<details>
  <summary>CSAM/SAM</summary>

Cualquier material que muestre explotación sexual de seres humanos. Tolerancia cero.

</details>

<details>
  <summary>Contenido ilegal</summary>

Contenido que viola la ley aplicable, como propaganda extremista, amenazas, discurso de odio, incitación a la violencia o difamación. Las variantes incluyen doxxing, amenazas explícitas y materiales prohibidos por la jurisdicción. Proporciona la ubicación exacta y, si se conoce, la base legal involucrada.

</details>

<details>
  <summary>Otro</summary>

Abuso que no encaja en lo anterior pero que aún perjudica a usuarios o sistemas. Ejemplos incluyen alojamiento de malware, botnet C2, fraude y minería de criptomonedas no autorizada. Comparte hashes, URLs, patrones de C2 y anomalías en el uso de recursos.

</details>

## Información requerida

Para asegurar un reporte completo y procesable, por favor proporciona detalles exhaustivos que nos permitan identificar el recurso, verificar el incidente y tomar las medidas adecuadas, incluyendo lo siguiente:
- Ubicación. URL, IP, puerto, nombre de host, ruta de archivo, hash
- Tiempos en UTC en formato YYYY-MM-DDTHH:MM:SSZ
- Descripción. Qué ocurrió, cómo se detectó, impacto observado
- Evidencia. Capturas de pantalla, registros de texto, correo electrónico completo con encabezados como EML, PCAP corto, NetFlow, encabezados HTTP

## Archivos aceptados y provisión

Proporciona la evidencia en formatos claros y de manera que podamos acceder a ella de forma confiable. Adjunta archivos pequeños a tu correo o aloja archivos grandes externamente. Adjunta archivos pequeños o medianos directamente. Prefiere formatos abiertos y sin modificar. El texto sin formato es mejor que capturas de pantalla de texto.

Para archivos grandes, comparte un enlace de descarga estable. Debe ser recuperable sin interacción o incluir credenciales claras. Indica la ventana de validez del enlace. Añade sumas de verificación para permitir la verificación de integridad.

Usa formatos estándar como TXT, PDF, PNG, JPG, PCAP o PCAPNG, EML, HAR, CSV y JSON. No incluyas contraseñas, claves privadas o datos personales completos a menos que sea estrictamente necesario.

Para calidad, envía correos electrónicos como EML con encabezados completos, registros como texto plano, trazas de red como capturas PCAP o PCAPNG cortas y relevantes, y capturas de pantalla en resolución original.

Por seguridad, redacta cualquier secreto; si es necesario, coloca los archivos en un archivo protegido por contraseña y comparte la contraseña por separado. Para CSAM/SAM, no transmitas archivos, proporciona solo enlaces.

## Ponte en contacto con nosotros

Envía tu reporte a `abuse@zap-hosting.com`. Es importante usar un asunto claro como `Reporte de Abuso Phishing` o `Reporte de Abuso DDoS`. Envía un correo por incidente. El siguiente ejemplo muestra una solicitud completa:

```
Para: abuse@zap-hosting.com
Asunto: Reporte de Abuso Fuerza Bruta (SSH)

Ubicación:
- IP objetivo: XXX.XX.XXX.XX
- Servicio: SSH
- Puerto: 22
- Nombre de host: v12345.zap-hosting.com

Tiempos (UTC):
- Primera detección: 2025-08-23T09:12:04Z
- Última detección: 2025-08-23T10:03:31Z

Descripción:
Intentos repetidos de inicio de sesión SSH con nombres de usuario e IPs de origen rotativos. Detectado por anomalías en auth.log y tasa elevada de conexiones. Autenticación por contraseña deshabilitada tras la detección. No se observó inicio de sesión exitoso.

Evidencia:
- Extracto de auth.log con múltiples entradas de "Failed password" y "Invalid user"
- Fragmento de registro de fail2ban mostrando bloqueos y direcciones de origen
- PCAP de 60 segundos capturando intentos TCP al puerto 22
- Conteos agregados: 12,438 intentos desde 352 IPs de origen
- Principales fuentes con información ASN

Ejemplo de registro:
2025-08-23T09:55:17Z sshd[2173]: Failed password for invalid user admin from XXX.X.XXX.XX port XXXX ssh2
2025-08-23T09:55:18Z sshd[2173]: Failed password for root from XXX.X.XX
```

## Qué sucede después

Nuestro Equipo de Abuso procesa tu reporte lo más rápido posible y responde prontamente. Revisamos el incidente y lo priorizamos según su gravedad.

Según la revisión, tomamos acciones que incluyen notificación al cliente, suspensión temporal/permanente, eliminación del contenido reportado, preservación de evidencia y notificación a las autoridades competentes cuando sea necesario.