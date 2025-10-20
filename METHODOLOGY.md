# Metodología - Casino Lab (SANITIZED)

## Fase 1 - Reconocimiento
- Escaneo de puertos y detección de servicios (`nmap`, `whatweb`).
- Enumeración de directorios (`gobuster`, `ffuf`).

## Fase 2 - Análisis de vulnerabilidades
- Identificar parámetros susceptibles a LFI.
- Usar LFI como vector para interactuar con servicios internos (SSRF-like).

## Fase 3 - Explotación
- Fuzz de puertos internos vía LFI para mapear servicios.
- Descargar artefactos accesibles (p. ej. claves privadas) solo en entorno controlado.

## Fase 4 - Post-explotación y Escalada
- Acceso inicial via SSH/key (si disponible en el laboratorio).
- Análisis de binarios locales (strings, objdump, radare2) para encontrar contraseñas/funciones.
- Explotación de file descriptors y técnicas de escalada documentadas.

## Fase 5 - Documentación y mitigaciones
- Reporte de hallazgos y recomendaciones (input sanitization, network segmentation, remove hardcoded creds).
