Descripción general del proyecto

El proyecto busca desarrollar un SCRIPT que combine PowerShell y Python para automatizar la recolección, filtrado y análisis de logs del sistema Windows.
El propósito es detectar eventos relevantes, errores críticos y posibles anomalías que puedan indicar fallos o actividades sospechosas, fortaleciendo las capacidades de monitoreo en un entorno de ciberseguridad.

Este proyecto se relaciona con las funciones de un SOC (Security Operations Center) y DFIR (Digital Forensics and Incident Response), aplicando principios éticos y técnicos del análisis de registros.

Ficha técnica de tareas
Tarea 1: Extracción de logs del sistema con PowerShell

Propósito: Automatizar la obtención de registros del sistema (seguridad, aplicación y sistema) desde el Visor de Eventos de Windows.
Área: SOC / Administración de sistemas.
Entradas esperadas: Comandos PowerShell como Get-WinEvent o Get-EventLog.
Salidas esperadas: Archivo .csv o .json con los registros filtrados.
Procedimiento: Filtrar logs por tipo, fecha o ID de evento y exportarlos.
Complejidad técnica: Media.
Controles éticos: Solo se usarán logs sintéticos en entornos de prueba.
Dependencias: PowerShell 5.1+, permisos de lectura del Visor de Eventos.

Tarea 2: Análisis de logs con Python

Propósito: Procesar los archivos exportados de PowerShell para identificar patrones, errores frecuentes y posibles amenazas.
Área: DFIR / SOC.
Entradas esperadas: Archivos .csv generados por PowerShell.
Salidas esperadas: Reportes .csv o .txt con resumen de eventos críticos y estadísticas.
Procedimiento: Leer los datos con pandas, filtrar eventos relevantes y generar reportes.
Complejidad técnica: Media–alta.
Controles éticos: Uso de datos anonimizados y sin información sensible.
Dependencias: Python 3.10+, librerías pandas, matplotlib.

Tarea 3: Integración del flujo completo

Propósito: Integrar los scripts de PowerShell y Python para automatizar el proceso completo de extracción y análisis.
Área: Automatización / SOC.
Entradas esperadas: Scripts individuales (extract_logs.ps1 y analyze_logs.py).
Salidas esperadas: Reporte final consolidado en /outputs.
Procedimiento: Ejecutar PowerShell, generar logs y luego analizar con Python automáticamente.
Complejidad técnica: Media.
Controles éticos: Solo ejecución en entornos de laboratorio.
Dependencias: PowerShell y Python instalados, permisos de ejecución de scripts.

Estructura inicial del repositorio
/proposals
 └── propuesta.md
/src
 ├── powershell/
 │   └── extract_logs.ps1
 ├── python/
 │   └── analyze_logs.py
/outputs
 ├── logs_filtrados.csv
 └── reporte_final.csv
/docs
 └── manual_uso.md
/examples
 └── ejemplo_logs.csv
README.md

Asignación de roles del equipo:
Integrante	Rol	Responsabilidades
Renata Alvarez del Castillo Garza	Coordinadora técnica y analista Python	Redacción de la propuesta, desarrollo del script Python, documentación.
Eva Rodriguez	Especialista PowerShell	Creación y pruebas del script de extracción de logs.
Sofia Perez	Analista DFIR	Validación de resultados y definición de eventos críticos.
Rene	Encargado del repositorio	Creación de carpetas y mantenimiento del GitHub.
Edgar	Gestor ético y de calidad	Redacción de la declaración ética y revisión del cumplimiento técnico.

Declaración ética y legal:
Este proyecto se realiza únicamente en entornos de prueba controlados, con datos sintéticos o anonimizados.
No se usarán sistemas reales, información sensible ni claves privadas.
El propósito es académico y formativo, promoviendo la ética y buenas prácticas en la ciberseguridad.

Evidencia de colaboración inicial:
Repositorio creado en GitHub con estructura definida.
Commits iniciales que muestran participación del equipo.
Issues o pull requests para coordinación.
Captura de pantalla enviada como evidencia en MS Teams.
