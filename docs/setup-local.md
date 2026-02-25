# Sintelo Core — Data Policy

## Principle
Este repositorio no debe contener datos sensibles de clientes.

## Allowed
— datos sintéticos o anonimizados  
— “golden outputs” pequeños para pruebas reproducibles  
— fixtures mínimos para validación

## Not Allowed
— dumps completos de ERP
— datasets con información identificable de clientes
— archivos pesados sin necesidad operativa

## Handling
Si se requiere manejar datos reales, se gestionarán fuera del repositorio y bajo controles de acceso definidos por Sintelo.
