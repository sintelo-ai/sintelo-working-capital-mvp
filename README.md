# Sintelo – Working Capital MVP

## What this is
This repository contains the MVP engine used to diagnose and govern working capital
in distribution businesses.

The goal is not reporting or BI.
The goal is to force explicit capital allocation decisions.

## What problem it solves
- Capital trapped in inventory
- Poor rotation at SKU level
- Implicit financing through customers and purchasing
- ROIC pressure driven by working capital misallocation

## Scope
Included:
- Inventory (SKU-level)
- Accounts receivable (or proxies in demo)
- Purchasing decisions
- Short-cycle capital release (30–90 days)

Excluded:
- Operational execution
- ERP implementation
- Full accounting accuracy
- Long-term transformations

## Data
- Demo data: AdventureWorks (transaction-level)
- Real use: ERP transactional data

## Outputs
- Decision tables (not dashboards)
- Capital-at-risk rankings
- Before / After capital simulations
- Operational ROIC (mandate-level)

## Philosophy
Imperfect but honest metrics that force decisions
beat perfect metrics that justify inaction.
