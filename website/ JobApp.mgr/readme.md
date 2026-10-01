# JobApp Manager

**Gestión integral de búsqueda de empleo — Aplicación web local, sin backend, 100% en el navegador.**

![SPA](https://img.shields.io/badge/SPA-Single%20Page%20Application-blue)
![LocalStorage](https://img.shields.io/badge/Persistencia-LocalStorage-yellow)
![Sin Backend](https://img.shields.io/badge/Backend-Ninguno-green)
![Licencia](https://img.shields.io/badge/Licencia-MIT-lightgrey)

---

## Tabla de contenidos

- [Descripción general](#descripción-general)
- [Capturas de pantalla](#capturas-de-pantalla)
- [Características](#características)
- [Modelo de datos](#modelo-de-datos)
- [Instalación y uso](#instalación-y-uso)
- Estructura del proyecto
- [Módulos](#módulos)
  - [Inicio (Dashboard)](#1-inicio-dashboard)
  - [Empresas](#2-empresas)
  - [Contactos](#3-contactos)
  - [Puestos](#4-puestos)
  - [Cartas de presentación](#5-cartas-de-presentación)
  - [Documentos](#6-documentos)
  - [Ajustes](#7-ajustes)
- [Reglas de borrado y cascada](#reglas-de-borrado-y-cascada)
- [Diseño y UX](#diseño-y-ux)
- [Persistencia y robustez](#persistencia-y-robustez)
- [Limitaciones conocidas](#limitaciones-conocidas)
- [Hoja de ruta](#hoja-de-ruta)
- [Licencia](#licencia)

---

## Descripción general

**JobApp Manager** es una aplicación web SPA (Single Page Application) pensada para organizar y centralizar todo el proceso de búsqueda de empleo: empresas, puestos, contactos, cartas de presentación y documentos (CVs, cartas motivacionales, notas, plantillas).

Toda la información se almacena en **localStorage** del navegador. No requiere servidor, base de datos externa ni cuenta de usuario. Abre el archivo HTML y empieza a trabajar.

### Filosofía

| Principio | Descripción |
|---|---|
| **Sin backend** | Cero dependencias de servidor. Todo corre en el navegador. |
| **Datos tuyos** | Toda la información vive en tu máquina. Exporta un JSON y llévatelo. |
| **Reutilización** | Cartas y documentos se asocian a múltiples puestos y empresas sin duplicar contenido. |
| **Minimalismo** | Interfaz azul/blanco, limpia, sin distracciones. |

---


## Características

- CRUD completo para **empresas**, **puestos**, **contactos**, **cartas de presentación** y **documentos**
- Asociación de cartas y documentos a empresas y puestos mediante **modales de selección**
- **Filtrado** de puestos por estado (Pendiente, Enviado, Entrevista, Oferta, Rechazado)
- **Filtrado** de cartas por tags
- **Filtrado** de documentos por tipo
- **Búsqueda** por texto en todos los listados
- **Duplicación** de cartas con un click
- **Versionado simple** de cartas: historial de contenido previo al editar
- **Cambio rápido de estado** en el detalle de puesto (botones por estado)
- **Exportación** de todos los datos a archivo `.json`
- **Importación** desde archivo `.json` (sobrescribe el estado actual)
- **Reset** completo de la aplicación con confirmación
- Persistencia automática en **localStorage** tras cada operación
- Estética **azul/blanco minimalista** con tipografía Plus Jakarta Sans
- Layout **split list/detail** para todas las vistas de datos
- **Modales** para formularios y selección de asociaciones
- **Toasts** para feedback visual de operaciones
- **Validación** de campos obligatorios en formularios

---

## Modelo de datos

Toda la aplicación persiste bajo una única clave de localStorage:
