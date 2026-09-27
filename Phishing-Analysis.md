# Phishing Analysis - Blue Team Labs Online Write-up

![Insignia de BTLO](/BTLO_Caso_1.jpeg)

## Introducción
Este es mi primer desafío resuelto en la plataforma Blue Team Labs Online (BTLO). El objetivo del laboratorio consistió en realizar un análisis técnico sobre un caso de sospecha de phishing, identificando los metadatos del correo, los enlaces maliciosos y la infraestructura involucrada.

Herramientas Utilizadas

    Mousepad: Editor de texto ligero para inspeccionar de forma segura las cabeceras y el cuerpo del archivo de correo .eml.
    URLScan.io: Sandbox web y plataforma de analisis para inspeccionar URLs sospechosas de manera aislada sin exponer el entorno de trabajo.

Paso a Paso del Analisis

1.  Inspeccion del Correo (.eml)
    Se procedio a abrir el archivo de correo adjunto utilizando el editor de texto Mousepad. Mediante el analisis directo de los encabezados y la funcion de busqueda (Ctrl + F), se ubicaron los metadatos clave:
    --> Identificacion de la direccion IP de origen y la fecha de envio del mensaje.
    --> Extraccion del nombre del archivo adjunto sospechoso (Website contact form submission.eml).
    --> Busqueda de la cadena http para extraer el enlace redirigido dentro del correo.

2.  Analisis del Enlace Sospechoso
    Una vez extraida la URL maliciosa que apuntaba a un subdominio de Blogspot, se utilizo URLScan.io para investigar el sitio de forma segura:
    --> Se verifico que el servicio de alojamiento correspondia a Blogspot.
    --> Se inspecciono la captura de pantalla (screenshot) y la seccion Page Title del reporte para confirmar el estado de la pagina.
    --> Se corroboro que el sitio ya figuraba fuera de linea con el mensaje de estado Blog has been removed / Blog not found.

Conclusion y Aprendizajes

Este laboratorio me permitio aplicar un flujo de trabajo analitico eficiente utilizando herramientas de entorno grafico (GUI) y plataformas en la nube. Aprendi la importancia de revisar el codigo fuente de un correo para encontrar Indicadores de Compromiso (IoC) y como utilizar plataformas de aislamiento para analizar enlaces peligrosos sin poner en riesgo la red.

Este write-up forma parte de mi portafolio continuo de aprendizaje en ciberseguridad defensiva (Blue Team).
