<div align="center">

<!-- CABECERA PRINCIPAL Y LOGO INTERACTIVO -->
<a href="https://github.com/RubenAcedo">
  <img src="https://capsule-render.vercel.app/api?type=waving&color=0d1117&height=220&section=header&text=RUBÉN%20ACEDO&fontSize=52&fontColor=ff0033&fontAlignY=42&desc=SOLUTIONS%20ARCHITECT%20%7C%20AI%20PIPELINES%20%7C%20WEB3%20SECURITY%20%7C%20BUILDER&descSize=14&descColor=e6edf3&descAlignY=64" width="100%"/>
</a>

<p align="center">
  <img src="https://img.shields.io/badge/NODE_STATUS-SYSTEM_OPERATIONAL-0d1117?style=for-the-badge&logo=statuspage&logoColor=00ff66" alt="Status"/>
  <img src="https://img.shields.io/badge/CORE-LOCAL_AI_AGENTICS-0d1117?style=for-the-badge&logo=python&logoColor=ff0033" alt="AI Agentics"/>
  <img src="https://img.shields.io/badge/SECURITY-MITRE_ATLAS_AUDITED-0d1117?style=for-the-badge&logo=hackthebox&logoColor=ff0033" alt="Security"/>
  <img src="https://img.shields.io/badge/EVM-SOLIDITY_RWA-0d1117?style=for-the-badge&logo=ethereum&logoColor=ffffff" alt="EVM"/>
</p>

<p align="center">
  <b>[ 🇪🇸 CONSOLA ESPAÑOL ]</b> &nbsp;•&nbsp; 
  <a href="./README.en.md"><b>[ 🇬🇧 ENGLISH MIRROR ]</b></a> &nbsp;•&nbsp; 
  <a href="#-matriz-curricular--cv-completo"><b>[ 📄 VER CV COMPLETO ]</b></a> &nbsp;•&nbsp; 
  <a href="mailto:tu-correo@dominio.com"><b>[ 📬 CONTACTO DIRECTO ]</b></a>
</p>

---

</div>

## 📺 Transmisión del Constructor: Visión & Trayectoria

<div align="center">

> *"Un sistema no se define por las librerías que importa, sino por la soberanía de sus datos, el rigor matemático de su lógica on-chain y la limpieza de su interfaz operativa."*

<!-- REPRODUCTOR VÍDEO DESTACADO -->
<a href="https://youtube.com/@Ostinia" target="_blank">
  <img src="https://img.shields.io/badge/REPRODUCIR_VÍDEO_DE_TRAYECTORIA-YouTube-ff0033?style=for-the-badge&logo=youtube&logoColor=white" height="38"/>
  <br/><br/>
  <img src="https://images.unsplash.com/photo-1550751827-4bd374c3f58b?auto=format&fit=crop&w=1200&q=80" alt="Video Pitch Play - Rubén Acedo" width="90%" style="border-radius: 8px; border: 2px solid #ff0033; box-shadow: 0 0 20px rgba(255,0,51,0.3);"/>
</a>

<br/>

<sub>💡 <i>Haz clic sobre la imagen para abrir la cápsula audiovisual en YouTube con el desglose de proyectos y enfoque técnico.</i></sub>

</div>

---

## ⚡ Panel de Navegación del Monorepo (Dashboard Operativo)

Haz clic en las tarjetas de la terminal para acceder a los módulos de código fuente:

<table>
<tr>
<td width="50%" valign="top">
  <div align="center">
    <img src="https://img.shields.io/badge/MODULE_01-AI_SYSTEMS-ff0033?style=flat-square&logo=cpu&logoColor=white"/>
    <h3>🧠 /ai-systems</h3>
    <p>Agentes autónomos locales, OpenCode, skills modulares y mitigación de fugas de datos mediante pipelines reproducibles.</p>
    <a href="./ai-systems">
      <img src="https://img.shields.io/badge/INSPECCIONAR_CÓDIGO-0d1117?style=for-the-badge&logo=github&logoColor=white"/>
    </a>
  </div>
</td>
<td width="50%" valign="top">
  <div align="center">
    <img src="https://img.shields.io/badge/MODULE_02-WEB3_ARCH-ff0033?style=flat-square&logo=ethereum&logoColor=white"/>
    <h3>⛓️ /web3</h3>
    <p>Contratos inteligentes en Solidity, tokenización de Real World Assets (RWA), control de acceso y suites de testing de invariantes.</p>
    <a href="./web3">
      <img src="https://img.shields.io/badge/AUDITAR_CONTRATOS-0d1117?style=for-the-badge&logo=solidity&logoColor=white"/>
    </a>
  </div>
</td>
</tr>
<tr>
<td width="50%" valign="top">
  <div align="center">
    <img src="https://img.shields.io/badge/MODULE_03-INTERFACES-111111?style=flat-square&logo=googlechrome&logoColor=ff0033"/>
    <h3>🖥️ /apps</h3>
    <p>Interfaces web tácticas, clientes ligeros para smart contracts y prototipos de interacción con agentes sin dependencias pesadas.</p>
    <a href="./apps">
      <img src="https://img.shields.io/badge/EXPLORAR_FRONTEND-0d1117?style=for-the-badge&logo=javascript&logoColor=white"/>
    </a>
  </div>
</td>
<td width="50%" valign="top">
  <div align="center">
    <img src="https://img.shields.io/badge/MODULE_04-TECHNICAL_DOCS-111111?style=flat-square&logo=gitbook&logoColor=ff0033"/>
    <h3>📑 /docs</h3>
    <p>Memorias de ingeniería, especificaciones formales, matrices de amenaza MITRE ATT&CK / ATLAS y diagramas de flujo.</p>
    <a href="./docs">
      <img src="https://img.shields.io/badge/LEER_MEMORIAS-0d1117?style=for-the-badge&logo=markdown&logoColor=white"/>
    </a>
  </div>
</td>
</tr>
</table>

---

## 🧭 Desglose Interactivo: Tesis, Arquitectura & Código

<details open>
<summary><b>[01] SISTEMAS DE IA: ORQUESTACIÓN LOCAL & AGENTES SOBERANOS</b></summary>
<br/>

> **Tesis:** La inteligencia artificial empresarial debe operar bajo soberanía de datos, ejecutándose en local sin filtrar secretos comerciales ni depender de APIs externas para tareas críticas de inferencia y análisis.

#### Diagrama de Flujo del Pipeline
```mermaid
graph LR
    subgraph Local_Host [Entorno Seguro Local]
        A[Input / Raw Task] --> B[OpenCode Orchestrator]
        B --> C{Ollama Local LLM}
        C -->|Skill Invocation| D[Python Automation Core]
        D -->|File / Data Operations| E[(Local Storage)]
        D --> F[Sanitized Output / Report]
    end
