# 🎰 Casino Lab - Writeup

![Pentest](https://img.shields.io/badge/Penetration-Test-red)
![Difficulty](https://img.shields.io/badge/Difficulty-Medium-orange)
![OS](https://img.shields.io/badge/OS-Linux-blue)

Una máquina Linux que simula un sistema de casino con múltiples vulnerabilidades que permiten escalar desde enumeración web hasta compromiso completo del sistema.

## 📋 Resumen

**Casino Lab** es una máquina vulnerable que presenta:
- Enumeración web con servicios expuestos
- Vulnerabilidad LFI (Local File Inclusion)
- Descubrimiento de servicios internos
- Fuga de credenciales SSH
- Binario con vulnerabilidad de file descriptor
- Escalada de privilegios

## 🎯 Estadísticas Rápidas

| Categoría | Detalles |
|-----------|----------|
| **Dificultad** | Media |
| **Sistema Operativo** | Linux (Debian) |
| **Servicios** | SSH (22), HTTP (80), Internal (6969) |
| **Técnicas** | LFI, SSRF, Password Cracking, Privilege Escalation |
| **Flags** | 2 (user.txt & root.txt) |

## 🚀 Empezar

```bash
# Clonar el repositorio
git clone https://github.com/jonathang88/casino-lab.git
cd casino-lab

# Ver la metodología completa
cat METHODOLOGY.md

# Leer el writeup detallado
cat writeup.md
