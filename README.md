# IC Chile — Infraestructura de Carga Pública

Pipeline de datos sobre la infraestructura pública de carga eléctrica
en Chile a partir de información declarada a la SEC, con limpieza,
agregaciones territoriales y un tablero exploratorio.

## Estado

🚧 En construcción.

## Stack técnico

- **Python 3.11**, **pandas**, **pyarrow** (Parquet)
- **DuckDB** para SQL local (proxy de BigQuery)
- **Streamlit** para el tablero
- **matplotlib**, **seaborn**, **plotly** para visualización
- **pytest** para tests
- **black** + **flake8** para estilo

## Estructura del proyecto
ic-chile/
├── data/
│   ├── bronze/     # Datos crudos, tal como vienen de la fuente
│   ├── silver/     # Datos limpios, tipos correctos, granularidad conector
│   └── gold/       # Datos agregados (por sitio, comuna, región)
├── notebooks/      # Exploración y prototipado (EDA)
├── src/            # Código Python reutilizable (limpieza, transformaciones)
├── sql/            # Queries SQL para DuckDB
├── app/            # Tablero Streamlit
├── tests/          # Tests con pytest
├── requirements.txt
└── README.md

## Cómo correr el proyecto

```bash
# Crear entorno virtual
python -m venv .venv

# Activar (Windows PowerShell)
.\.venv\Scripts\Activate.ps1

# Instalar dependencias
pip install -r requirements.txt
```

## Fuente de datos

Base de datos pública de infraestructura de carga declarada ante la
Superintendencia de Electricidad y Combustibles (SEC), con granularidad
a nivel de conector.

## Autor

Josue Muñoz · 2026