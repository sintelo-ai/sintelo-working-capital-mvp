# Sintelo Core — Runbook

## 1. Purpose

Este documento define el procedimiento oficial para ejecutar el pipeline analítico de Sintelo Core.

El objetivo es asegurar ejecución reproducible, consistente y auditable.

Este runbook constituye la referencia operativa institucional.

---

## 2. Execution Overview

Sintelo Core se ejecuta mediante una secuencia de notebooks estructurados bajo metodología CRISP-DM.

Flujo institucional:

Business Understanding  
→ Data Understanding  
→ Data Preparation  
→ Modeling  
→ Evaluation  
→ Gold Layer  
→ Outputs  

---

## 3. Preconditions

Antes de ejecutar, verificar:

— entorno virtual activo  
— dependencias instaladas  
— acceso a carpeta `/data`  
— carpeta `/outputs` accesible  

Activar entorno virtual:

```bash
source venv/bin/activate
