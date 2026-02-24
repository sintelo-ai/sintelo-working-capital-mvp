# Sintelo Core — Repository Map

## Purpose

Este repositorio contiene Sintelo Core, el motor propietario de análisis financiero y creación de valor de Sintelo.

El sistema transforma datos operativos y contables en outputs analíticos estructurados utilizados para evaluación financiera y toma de decisiones.

Este documento describe la organización institucional del repositorio.

---

## Top-Level Structure

### /architecture

Contiene la definición formal de la arquitectura del sistema.

Incluye:

— estado actual del sistema  
— arquitectura objetivo  
— flujo de datos  
— contratos entre componentes  

Esta carpeta define cómo el sistema está y cómo debe evolucionar.

---

### /core

Contiene la definición conceptual del motor Sintelo Core.

Incluye:

— descripción del motor  
— modelo de dominio financiero  
— contratos de outputs  
— estándares de calidad institucional  

No contiene la implementación técnica directa.

---

### /docs

Contiene documentación operativa y técnica para uso interno.

Incluye:

— instrucciones de setup  
— guías de ejecución  
— troubleshooting  
— documentación de soporte  

Esta carpeta permite que el sistema sea operable por nuevos miembros del equipo.

---

### /governance

Contiene la definición de gobernanza institucional del sistema.

Incluye:

— ownership del activo  
— políticas de acceso  
— control de cambios  
— estándares de seguridad  

Esta carpeta define cómo se controla y protege el sistema.

---

### /config

Contiene archivos de configuración utilizados por el sistema.

Incluye:

— parámetros de ejecución  
— configuraciones de entorno  
— mapeos y supuestos configurables  

La configuración está separada del código para permitir flexibilidad y control.

---

### /data

Contiene datasets de trabajo utilizados durante el procesamiento.

Incluye:

— datos de prueba  
— datasets intermedios  
— fixtures reproducibles  

No debe contener datos sensibles sin anonimización.

---

### /notebooks

Contiene la implementación analítica funcional actual del pipeline.

Estos notebooks ejecutan el procesamiento completo de datos y constituyen el motor operativo actual del sistema.

Esta capa será progresivamente modularizada.

---

### /src

Contiene componentes de código modular reutilizable.

Esta carpeta representa la dirección futura del motor institucional, donde la lógica será encapsulada en módulos versionables y desplegables.

---

### /outputs

Contiene outputs generados por el motor.

Incluye artefactos analíticos utilizados para validación, revisión y consumo interno.

---

### requirements.txt

Define las dependencias técnicas necesarias para ejecutar el sistema.

---

### README.md

Define el propósito institucional del sistema y su rol dentro de Sintelo.

---

## Institutional Principle

Sintelo Core es un activo institucional.

El repositorio está estructurado para:

— asegurar continuidad operativa  
— permitir evolución controlada  
— facilitar onboarding técnico  
— preservar integridad del sistema  

Todos los cambios deben respetar esta estructura.
