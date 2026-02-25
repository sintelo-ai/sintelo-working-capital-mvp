# Sintelo Core — Head of Engineering Onboarding

## 1. Purpose

Este documento define el onboarding técnico oficial para el Head of Engineering de Sintelo.

El objetivo es transferir contexto, responsabilidad y dirección técnica sobre Sintelo Core como activo institucional.

Sintelo Core constituye el motor propietario de análisis financiero de la firma.

---

## 2. Role Definition

El Head of Engineering es responsable de:

— estabilidad técnica del sistema  
— evolución de la arquitectura  
— implementación de la arquitectura objetivo  
— preparación para operación multi-cliente  
— asegurar reproducibilidad y auditabilidad  

El rol no es crear un sistema nuevo.

El rol es institucionalizar el sistema existente.

---

## 3. First Principle

Sintelo Core es un activo institucional existente.

El sistema actual es funcional.

La prioridad es preservar funcionalidad mientras se evoluciona arquitectura.

No se permite reescritura completa sin justificación técnica documentada.

La evolución debe ser incremental.

---

## 4. Repository Familiarization

El primer paso es revisar el repositorio completo.

Orden de lectura obligatorio:

1.

README.md

2.

docs/repo-map.md

3.

docs/setup-local.md

4.

docs/runbook.md

5.

architecture/current-architecture.md

6.

architecture/target-architecture.md

7.

core/engine-overview.md

8.

governance/ownership.md

---

## 5. System Execution

El Head of Engineering debe ejecutar Sintelo Core localmente.

Seguir:

docs/setup-local.md

Luego:

docs/runbook.md

Objetivo:

Confirmar que el sistema:

— ejecuta correctamente  
— genera Gold Layer  
— genera outputs  

Esto establece comprensión operativa.

---

## 6. System Understanding Deliverable

Dentro de los primeros 14 días, el Head of Engineering debe producir:

Sintelo Core — Technical Assessment Memo

Contenido requerido:

— evaluación de arquitectura actual  
— riesgos técnicos  
— deuda técnica  
— recomendaciones  

Este documento establece la base técnica institucional.

---

## 7. Architectural Responsibility

El Head of Engineering será responsable de implementar:

architecture/target-architecture.md

Esto incluye:

— migración progresiva desde notebooks hacia src/  
— implementación de ingestion layer  
— automatización del pipeline  
— preparación para deployment  

---

## 8. Operational Responsibility

Responsabilidades continuas:

— asegurar reproducibilidad  
— prevenir degradación del sistema  
— mantener documentación actualizada  
— establecer estándares técnicos  

---

## 9. Change Management

Todo cambio significativo debe:

— ser documentado  
— preservar outputs institucionales  
— no romper compatibilidad sin justificación  

La estabilidad del sistema es prioritaria.

---

## 10. Technology Direction

Stack actual:

Python  
Parquet  
Notebooks  

Stack objetivo:

Python modular  
Cloud execution  
Automated pipeline  

La evolución será progresiva.

---

## 11. Institutional Principle

Sintelo Core es un activo institucional.

El Head of Engineering es custodio técnico.

La propiedad reside en Sintelo.

Ver:

governance/ownership.md

---

## 12. First 30-Day Objectives

Objetivos iniciales:

1.

Comprender completamente el sistema

2.

Ejecutar el pipeline end-to-end

3.

Identificar riesgos técnicos

4.

Producir Technical Assessment Memo

5.

Proponer roadmap técnico

---

## 13. Long-Term Objective

El objetivo es transformar Sintelo Core en un motor institucional automatizado capaz de operar a escala multi-cliente.

El Head of Engineering liderará esta evolución.

---

## 14. Summary

Responsabilidad principal:

Preservar, institucionalizar y escalar Sintelo Core.

Este documento constituye la referencia oficial de onboarding técnico.
