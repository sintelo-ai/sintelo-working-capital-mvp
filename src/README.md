# Sintelo Core — src/

## Purpose

Este directorio contiene la implementación modular del motor institucional de Sintelo Core.

La evolución del sistema migrará progresivamente la lógica crítica desde notebooks hacia módulos versionables y testeables aquí.

## What belongs here

— ingestion connectors (cuando existan)  
— normalización y transforms  
— construcción del Gold Layer  
— lógica de métricas financieras  
— generación de outputs estructurados  
— validaciones y controles de calidad

## What does NOT belong here

— notebooks (viven en /notebooks)  
— datasets (viven en /data)  
— outputs generados (viven en /outputs)

## Institutional principle

No se permite duplicar lógica en notebooks y src sin plan de migración documentado.
