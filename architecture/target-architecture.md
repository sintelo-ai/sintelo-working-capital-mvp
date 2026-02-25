# Sintelo Core — Target Architecture (v1)

## 1. Purpose

Este documento define la arquitectura objetivo de Sintelo Core.

El propósito es evolucionar el sistema actual, basado en notebooks reproducibles, hacia un motor institucional modular, automatizado y multi-cliente, preservando compatibilidad con el Gold Layer existente.

La arquitectura objetivo constituye la referencia técnica oficial para la evolución del sistema.



## 2. Architectural Principles

Sintelo Core deberá cumplir los siguientes principios:

Reproducible
Los mismos inputs deben producir los mismos outputs.

Determinístico
La lógica financiera no debe depender de ejecución manual.

Auditable
Cada dataset Gold debe poder rastrearse a su fuente y transformaciones.

Modular
La lógica debe vivir en módulos versionables bajo /src.

Incremental
La migración desde notebooks debe ser progresiva, sin reescrituras totales.

ERP-agnostic
El modelo institucional (Gold Layer) no depende de un ERP específico.

Multi-client ready
El sistema debe poder ejecutar aisladamente por cliente.



## 3. Conceptual Data Flow

Flujo institucional objetivo:

Source Systems (ERP, CSV, APIs)
↓
Ingestion Layer
↓
Raw Layer (immutable copy)
↓
Processing Layer (normalization)
↓
Gold Layer (institutional model)
↓
Analysis Layer
↓
Outputs Layer
↓
Applications (reports, dashboards)



## 4. Layer Definitions

4.1 Ingestion Layer

Responsabilidad:

Extraer datos desde sistemas fuente.

Fuentes objetivo incluyen:
	•	ERPNext
	•	SAP
	•	Odoo
	•	Microsoft Dynamics
	•	CONTPAQi
	•	archivos CSV / Excel

Implementación objetivo:

src/ingestion/

Output:

Datasets estructurados en Raw Layer.



4.2 Raw Layer

Responsabilidad:

Almacenar copia inmutable de datos fuente.

Características:
	•	Sin transformación
	•	Versionado
	•	Trazabilidad completa

Ubicación típica:

data/raw/

Nota:

Este layer no es utilizado directamente para análisis financiero.



4.3 Processing Layer

Responsabilidad:

Transformar Raw → datasets normalizados.

Incluye:
	•	limpieza
	•	validación
	•	estandarización

Implementación objetivo:

src/processing/

Output:

Datasets listos para modelado institucional.

Este layer es equivalente funcional al contenido actual de:

notebooks/03_data_preparation.ipynb



4.4 Gold Layer (Institutional Data Model)

Responsabilidad:

Definir el modelo de datos institucional de Sintelo.

Este es el layer más importante del sistema.

Ejemplo actual:

data/gold/inventory_gold_YYYY-MM-DD.parquet

El Gold Layer representa:
	•	posición financiera institucional
	•	capital invertido
	•	working capital
	•	métricas propietarias

Definiciones formales viven en:

core/gold-contracts.md

Implementación objetivo:

src/gold/



4.5 Analysis Layer

Responsabilidad:

Consumir Gold Layer y producir artefactos analíticos.

Incluye:
	•	generación de contextos
	•	cálculo de métricas
	•	preparación de outputs

Implementación objetivo:

src/analysis/

Este layer corresponde actualmente a:

notebooks/05_evaluation.ipynb



4.6 Outputs Layer

Responsabilidad:

Almacenar artefactos institucionales generados.

Ubicación:

outputs/
notebooks/reports/

Ejemplos:
	•	context_YYYY-MM-DD.json
	•	facts_pack_YYYY-MM-DD.json
	•	inventory_capital_memo_YYYY-MM-DD.txt

Estos archivos constituyen entregables institucionales.



4.7 Application Layer

Responsabilidad:

Consumir outputs del motor.

Ejemplos:
	•	dashboards
	•	reportes
	•	herramientas internas

Este layer está fuera del alcance directo de Sintelo Core.

Sintelo Core es el motor, no la interfaz.



## 5. Repository Target Structure

Estructura objetivo del repositorio:

architecture/
core/
config/
data/
docs/
governance/

src/
 ingestion/
 processing/
 gold/
 analysis/

notebooks/
outputs/

Los notebooks permanecerán como:
	•	entorno de investigación
	•	validación
	•	prototipado

No como capa operativa principal.



## 6. Execution Model

Estado actual:

Ejecución manual vía notebooks.

Estado objetivo:

Ejecución vía módulos Python.

Ejemplo:

python -m src.gold.inventory

Posteriormente:
	•	ejecución automatizada
	•	ejecución programada
	•	operación institucional



## 7. Multi-Client Architecture

Sintelo Core deberá soportar múltiples clientes.

Principios:
	•	aislamiento de datasets
	•	ejecución independiente
	•	outputs independientes

Conceptualmente:

data/clients/client_a/
data/clients/client_b/
data/clients/client_c/

Compartiendo la misma lógica institucional.



## 8. Migration Strategy

La migración se ejecutará en fases:

Phase 1 — Encapsulation
Extraer lógica desde notebooks hacia src/ sin cambiar outputs.

Phase 2 — Modularization
Separar ingestion, processing, gold, analysis.

Phase 3 — Automation
Eliminar dependencia operativa de notebooks.

Phase 4 — Deployment
Ejecutar sistema en entorno institucional automatizado.



## 9. Backward Compatibility Requirement

Durante la migración:

El Gold Layer actual debe permanecer compatible.

No se permite romper:

data/gold/

sin versionado explícito.



## 10. Role of Head of Engineering

El Head of Engineering será responsable de:
	•	ejecutar esta arquitectura
	•	liderar la migración técnica
	•	asegurar estabilidad institucional

Este documento constituye la referencia oficial.



## 11. Long-Term Objective

El objetivo final es que Sintelo Core opere como un motor institucional automatizado capaz de:
	•	ingerir datos multi-ERP
	•	producir el modelo institucional (Gold Layer)
	•	generar outputs analíticos
	•	operar sin intervención manual

Sintelo Core constituye el núcleo técnico de Sintelo.



## 12. Summary

Arquitectura objetivo:

ERP → Raw → Processing → Gold → Analysis → Outputs

Donde:

Gold Layer = modelo institucional de Sintelo

Este documento define el estado objetivo oficial del sistema.
