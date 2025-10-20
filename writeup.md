# Casino Lab - Writeup (SANITIZED)

## Introducción
Casino Lab simula un sistema con múltiples vulnerabilidades: LFI, servicios internos expuestos, exposición de credenciales y un binario vulnerable. Este writeup describe los pasos de manera educativa y con contenido sanitizado.

## Resumen de la cadena de explotación (sanitized)
1. Reconocimiento: detección de HTTP and endpoints with LFI-like behavior.
2. Identificación de parámetro vulnerable en `/casino/explainmepls.php`.
3. Uso de LFI para realizar fuzzing de puertos internos y descubrir un servicio en un puerto no estándar.
4. Extracción de archivos expuestos por el servicio interno (llaves/credenciales) — removidas en este repo.
5. Acceso inicial (SSH/key) en entorno de laboratorio.
6. Análisis de un binario local con cadenas y técnicas de reverse engineering para encontrar contraseñas (redacted).
7. Explotación de file descriptors para obtener información adicional y escalada a root (demonstrative).
8. Obtención de flags en el laboratorio (flags removed).

## Recomendaciones de seguridad
- Deshabilitar LFI or apply strict input sanitization and whitelisting.
- Network segmentation to prevent internal service exposure.
- Avoid hardcoding credentials; use secure vaults.
- Review file permissions and access to file descriptors.
- Monitor and audit access to critical files.
