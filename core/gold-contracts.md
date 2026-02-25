# Sintelo Core — Gold Contracts (v0)

## Purpose
Definir contratos mínimos de las tablas Gold institucionales. Gold es el modelo de datos institucional de Sintelo.

## Gold: Inventory

### Dataset
inventory_gold_YYYY-MM-DD.parquet

### Minimum Columns (v0)
— as_of_date  
— sku_id (o item_code)  
— location_id (si aplica)  
— quantity_on_hand  
— unit_cost  
— inventory_value  
— currency  
— source_system  
— load_timestamp  

### Rules
— inventory_value = quantity_on_hand * unit_cost  
— unit_cost debe estar en moneda base definida por configuración  
— keys deben ser estables (sku_id + location_id + as_of_date)

### Notes
Las columnas exactas pueden evolucionar, pero no se debe romper compatibilidad sin versionado explícito.
