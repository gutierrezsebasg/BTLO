# PowerShell Analysis - Keylogger

![](./img/BTLO_Caso_2.jpeg)

## Introducción
Mi segundo lab. Un script de PowerShell que era un keylogger.

## Herramientas que usé
- Terminal Kali: `unzip` y `sha256sum`
- Mousepad

## Qué hice
Descomprimí el zip con `infected`, saqué el hash y abrí el .ps1 con Mousepad. Busqué el email, el puerto y la DLL con Ctrl+F.

## IoCs que encontré
- Hash SHA256: e0b7a2ad2320ac32c262aeb6fe2c6c0d75449c6e34d0d18a531157c827b9754e
- DLL: user32.dll
- Ruta: $env:temp\keylogger.txt
- Puerto SMTP: 587

## Qué aprendí
Aprendí a encontrar credenciales y rutas rápido dentro de un script malicioso.
