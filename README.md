# ETL / Data Warehouse On-Premise

Este repositorio documenta una arquitectura ETL y Data Warehouse implementada on-premise, diseñada para la ingesta, transformación, almacenamiento y análisis de datos provenientes de múltiples fuentes.

## 🧱 Arquitectura General

La arquitectura está compuesta por los siguientes bloques:

- **Fuentes de Datos**: Bases de datos y APIs.
- **Ingesta**: Scripts Python para extracción, orquestados por Apache Airflow.
- **Staging y Transformación**: PostgreSQL como zona de staging + notebooks para limpieza y transformación.
- **Data Warehouse (DWH)**: Repositorio central en PostgreSQL.
- **Data Marts**: Subdivisiones del DWH orientadas al negocio.
- **BI**: Herramientas como Power BI para visualización y análisis.

## 🔁 Flujo de Datos (ETL)

1. **Extracción** desde fuentes externas.
2. **Ingesta** y validación preliminar.
3. **Transformación** en zona de staging.
4. **Carga** a DWH.
5. **Distribución** a Data Marts.
6. **Consumo BI**.

## 📁 Estructura del Repositorio

```bash
etl-warehouse-architecture/
├── README.md                  # Documentación principal
├── docs/
│   └── arquitectura_etl_on_premise.md  # Documento detallado de arquitectura
├── dags/                      # DAGs de Apache Airflow
├── scripts/                   # Scripts de ingesta y transformación
├── notebooks/                 # Notebooks de transformación/validación
└── config/                    # Configuraciones del entorno (ej. Airflow)
```

## 🚀 Requisitos Técnicos
- Python >= 3.8
- PostgreSQL >= 12
- Apache Airflow >= 2.x
- Jupyter o entorno similar
- Power BI (opcional para visualización)


## ✍️ Autores

Diego Huaman Mayanga
