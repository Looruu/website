<div align="center">

# Rubén Acedo

### Solutions Architect · AI Systems Engineering & Smart Contract Architecture
*Designing verifiable on-chain logic, local agent pipelines, and secure data infrastructures.*

---

[![Licencia](https://img.shields.io/badge/License-Apache--2.0-0969da?style=flat-square)](LICENSE)
[![Solidity](https://img.shields.io/badge/Solidity-0.8.24-363636?style=flat-square&logo=solidity&logoColor=white)](./web3)
[![Python](https://img.shields.io/badge/Python-3.11+-3776AB?style=flat-square&logo=python&logoColor=white)](./ai-systems)
[![Security Standards](https://img.shields.io/badge/Security-MITRE%20ATLAS%20%7C%20ATT%26CK-cf222e?style=flat-square)](./docs)

<br/>

[ 🇪🇸 Documentación en Español ] &nbsp;•&nbsp; [ 🇬🇧 [English Specification](./README.en.md) ] &nbsp;•&nbsp; [ 📋 [Curriculum Vitae](#-curriculum-vitae-ejecutivo) ] &nbsp;•&nbsp; [ 📬 [Contacto](#-contacto-profesional) ]

</div>

---

## Executive Summary

Profesional multidisciplinar especializado en el diseño e implementación de sistemas de software donde convergen la **inteligencia artificial soberana (local-first)** y la **arquitectura descentralizada sobre EVM**. 

Enfoque integral en el ciclo de vida del software: desde el modelado formal de especificaciones y análisis de vectores de ataque (threat modeling) hasta la implementación de smart contracts con cobertura exhaustiva de invariantes e interfaces operativas de baja latencia.

---

## Technical Overview (Monorepo Architecture)

Este repositorio centraliza implementaciones auditables, contratos en producción/testnet y pipelines reproducibles.
---

## Core Domains & Production Deliverables

### 1. Inferencia Local y Orquestación de Agentes (`/ai-systems`)
Arquitectura orientada a la soberanía del dato, evitando la dependencia de APIs cerradas y mitigando riesgos de fuga de telemetría o propiedad intelectual.
* **Componentes:** Integración de modelos abiertos vía Ollama, pipelines desacoplados en Python y entornos configurables en OpenCode.
* **Seguridad:** Sanitización de prompts en tiempo de ejecución para mitigar vectores de inyección indirecta (`MITRE ATLAS AML.T0015`).
* 📁 **[Explorar código y especificaciones en `/ai-systems` →](./ai-systems)**

### 2. Arquitectura de Smart Contracts & Tokenización (`/web3`)
Implementación de primitivas on-chain auditables y seguras, modeladas para casos de uso de tokenización de activos del mundo real (RWA) y tesorerías descentralizadas.
* **Componentes:** Contratos en Solidity compilados con optimización de gas, patrones de control de acceso basados en roles (RBAC) y guardas contra reentrancia.
* **Testing:** Cobertura de tests unitarios y fuzz testing para validación estricta de invariantes.
* 📁 **[Auditar código fuente y tests en `/web3` →](./web3)**

### 3. Interfaces Operativas (`/apps`)
Desarrollo de frontends funcionales que eliminan dependencias innecesarias, garantizando tiempos de carga óptimos y comunicación directa vía RPC y REST.
* 📁 **[Consultar implementaciones en `/apps` →](./apps)**

### 4. Investigación y Especificación Técnica (`/docs`)
Documentación formal de arquitecturas, diagramas de flujo de datos y análisis de amenazas según marcos MITRE ATT&CK y MITRE ATLAS.
* 📁 **[Leer especificaciones y memorias en `/docs` →](./docs)**

---

## Presentación Técnica & Trayectoria

<div align="center">

[![Video Overview](https://img.shields.io/badge/Ver_Presentación_Técnica-YouTube-0969da?style=for-the-badge&logo=youtube&logoColor=white)](https://youtube.com/@Ostinia)

<br/>

*Desglose en vídeo sobre arquitectura de sistemas, filosofía de construcción y visión técnica.*

</div>

---

## 📋 Curriculum Vitae Ejecutivo

<details open>
<summary><b>Experiencia Profesional y Proyectos Técnicos</b></summary>
<br/>

#### Lead Solutions Architect & Fundador · Ostinia Academy
*2024 — Presente*
* Diseño y despliegue de arquitecturas de software orientadas a IA soberana, desarrollo seguro de smart contracts y automatizaciones avanzadas.
* Creación de pipelines de desarrollo local asistido con OpenCode y modelos cuantizados locales.
* Elaboración de modelos de tokenización de activos del mundo real (RWA) y redacción de especificaciones técnicas formales.

#### Consultor Independiente de Automatización y Arquitectura Técnica
*2022 — Presente*
* Desarrollo de scripts en Python para ingesta, transformación y persistencia estructurada de datos.
* Modelado de matrices de riesgo e implementación de mitigaciones de seguridad contra prompt injections en sistemas impulsados por LLMs.
* Integración de interfaces web ligeras con persistencia local y conectividad Web3.

#### Dirección Operativa & Gestión de Proyectos Técnicos
*Trayectoria consolidada previa*
* Más de una década liderando proyectos de alta precisión técnica y visual, gestionando flujos de entrega continuos y optimización de recursos.
</details>

<details open>
<summary><b>Educación Formal y Especializaciones</b></summary>
<br/>

* **Máster en Blockchain y Criptoactivos:** IEBS Digital School
  * *Especialización:* Arquitectura EVM, diseño de smart contracts en Solidity, modelos DeFi y gobernanza tokenizada.
* **Formación Avanzada en Ciberseguridad e Inteligencia Artificial:** Security Academy
  * *Especialización:* Threat Intelligence (CTI), marcos MITRE ATT&CK y MITRE ATLAS, seguridad en modelos fundacionales.
* **Ingeniería de Software & Arquitectura de Sistemas:** Formación continua y aplicada en sistemas distribuidos, Linux y pipelines en Python.
</details>

<details open>
<summary><b>Matriz de Habilidades Técnicas</b></summary>
<br/>

| Dominio | Tecnologías y Metodologías |
| :--- | :--- |
| **Inteligencia Artificial** | Python, Ollama, OpenCode, Agentes Modulares, Inferencia Local, Prompt Hardening |
| **Blockchain / EVM** | Solidity, Foundry, Hardhat, OpenZeppelin, Tokenización RWA, Gas Optimization |
| **Ciberseguridad** | Threat Modeling, MITRE ATT&CK, MITRE ATLAS, Sanitización de I/O, Auditoría Estática |
| **Infraestructura & Web** | Linux/UNIX, Bash, GitOps, Docker, HTML5/Modern JS, REST APIs, CI/CD |

</details>

---

## 📬 Contacto Profesional

Disponible para roles de arquitectura técnica, desarrollo de infraestructura Web3 e integración de agentes de IA:

* **LinkedIn:** [linkedin.com/in/rubenacedo](https://linkedin.com)
* **Correo Electrónico:** [contacto@rubenacedo.com](mailto:contacto@rubenacedo.com)
* **Repositorio de Proyectos:** [github.com/RubenAcedo](https://github.com)
