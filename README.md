<div align="center">

# 📧 Automatización de Excel con Python

**Lee una planilla de ventas y envía por mail un reconocimiento a quienes superan una meta.**

![Python](https://img.shields.io/badge/Python-3-3776AB?style=flat-square&logo=python&logoColor=white)
![openpyxl](https://img.shields.io/badge/openpyxl-Excel-217346?style=flat-square&logo=microsoftexcel&logoColor=white)
![SMTP](https://img.shields.io/badge/email-SMTP-EA4335?style=flat-square&logo=gmail&logoColor=white)

</div>

## Qué resuelve

Revisar una planilla fila por fila y avisar a cada vendedor es una tarea repetitiva. El script la automatiza: recorre `ventas.xlsx` y, a cada persona con ventas superiores a **3000**, le manda un mail de felicitación.

## Formato de la planilla

La primera fila es el encabezado. Las columnas esperadas son:

| Nombre | Email | Venta |
|---|---|---|
| Ana | ana@ejemplo.com | 4200 |

Se incluye `ventas.xlsx` como ejemplo.

## Cómo usarlo

```bash
pip install openpyxl

# Credenciales por variables de entorno (nunca en el código)
export EMAIL_REMITENTE="tu_cuenta@gmail.com"
export EMAIL_PASSWORD="contraseña-de-aplicación"   # Windows PowerShell: $env:EMAIL_PASSWORD="..."

python codigo.py
```

> Con Gmail hay que usar una **contraseña de aplicación** (requiere verificación en dos pasos), no la contraseña de la cuenta.

## Stack

Python · `openpyxl` (lectura de Excel) · `smtplib` y `email.mime` (envío por SMTP)

## Ideas para mejorarlo

- Umbral de venta configurable.
- Plantilla de mensaje y modo de prueba que no envíe mails reales.
- Registro de los envíos realizados.

## Autora

**Carolina Lobo** · [LinkedIn](https://www.linkedin.com/in/carolina-lobo-469705297)
