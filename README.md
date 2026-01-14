# ProyectoVIPOWERBI

📊 Airbnb Global Benchmarking - Power BI

Este proyecto presenta un análisis de competitividad para alojamientos Airbnb en determoinadas ciudades (Madrid, Nueva York, Londres, Milán, Tokio y Sydney). El objetivo es identificar barrios con alta rentabilidad y demanda mediante métricas comparativas.

🛠️ Proceso ETL y Limpieza (Power Query)

    Conexión: Importación y consolidación de 6 fuentes CSV independientes.

    Limpieza: * Normalización de tipos de datos (Precios a currency/decimal, IDs a texto, fechas a date, etc).

        Eliminación de nulos en campos críticos (Price, Neighbourhood).

        Filtrado de outliers (registros con precio 0).

    Transformación: Creación de columna dinámica de Ciudad y una tabla de Listings_FActs para permitir el filtrado global y unificación de los datos sin necesidad de fusionar las tablas originales.

📐 Modelo de Datos

    Esquema: Integración de tablas de hechos (Fact_Listings) con tabla de medidas técnicas.

    Medidas DAX Clave:

        Total Listings: Conteo de oferta disponible.

        Average Price: Coste medio por noche.

        Est. Occupancy %: Ratio basado en disponibilidad anual.

        City Rank: Ranking dinámico de barrios por competitividad de precio (Average price rank ordenado de menor a mayor.

📈 Dashboard Interactivo

El informe en Report View consta de:

    Panel de KPIs: Tarjetas con métricas principales (Revenue estimada, Ocupación de airbnb's estimada, etc.) filtradas por ciudad.

    Análisis Geoespacial: Mapa que cruza volumen de oferta y precio medio.

    Distribución de Mercado: Gráfico que cruza el tipo de propiedad y el número minimo de noches que tienes que estar en ella.

    Benchmarking de Barrios: Gráfico de barras con el Top 10 de zonas más económicas/rentables.
