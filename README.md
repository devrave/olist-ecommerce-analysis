# olist-ecommerce-analysis
# 🛒 Olist E-Commerce Analysis

![Python](https://img.shields.io/badge/Python-3.8%2B-blue)
![Pandas](https://img.shields.io/badge/Pandas-2.1.4-green)
![Power BI](https://img.shields.io/badge/Power%20BI-Latest-yellow)
![License](https://img.shields.io/badge/License-MIT-red)

## 📊 Proyecto de Análisis de Datos E-Commerce

Análisis completo del dataset **Brazilian E-Commerce (Olist)** utilizando Python para el análisis de datos y Power BI para la visualización interactiva.

Este proyecto forma parte de mi portafolio de Data Analytics y demuestra habilidades en:
- 🐍 **Python**: Pandas, NumPy, Scikit-learn
- 📈 **Visualización**: Matplotlib, Seaborn, Plotly
- 💼 **Power BI**: Dashboards interactivos
- 📊 **Análisis**: RFM, Segmentación, Predicción
- 🧹 **Data Engineering**: ETL, Feature Engineering

---

## 🎯 Objetivos del Proyecto

### Business Questions

**Análisis de Ventas:**
- ¿Cuál es la tendencia de ventas a lo largo del tiempo?
- ¿Cuáles son los productos y categorías más rentables?
- ¿Cuál es el Average Order Value (AOV)?
- ¿Cómo se distribuyen las ventas geográficamente?

**Análisis de Clientes:**
- ¿Cómo segmentamos a los clientes usando RFM?
- ¿Cuál es el Customer Lifetime Value (CLV)?
- ¿Qué porcentaje de clientes son recurrentes?

**Análisis de Satisfacción:**
- ¿Qué factores influyen en el review score?
- ¿Cómo impacta el tiempo de entrega en la satisfacción?

**Análisis Predictivo:**
- Predicción de ventas futuras
- Predicción de satisfacción del cliente

---

## 📁 Estructura del Proyecto

```
olist-ecommerce-analysis/
├── 📁 data/
│   ├── raw/                          # Datos originales de Olist
│   ├── processed/                    # Datos procesados
│   └── README.md                     # Diccionario de datos
│
���── 📁 notebooks/
│   ├── 00_data_understanding.ipynb   # Exploración inicial del dataset
│   ├── 01_data_cleaning.ipynb        # Limpieza y preparación
│   ├── 02_eda.ipynb                  # Análisis exploratorio
│   ├── 03_sales_analysis.ipynb       # Análisis de ventas
│   ├── 04_customer_rfm.ipynb         # Segmentación RFM
│   ├── 05_sentiment_analysis.ipynb   # Análisis de reviews
│   └── 06_predictive_model.ipynb     # Modelos predictivos
│
├── 📁 src/
│   ├── data_loader.py                # Funciones para cargar datos
│   ├── data_cleaner.py               # Funciones de limpieza
│   ├── feature_engineering.py        # Creación de features
│   ├── rfm_analysis.py               # Análisis RFM
│   ├── visualizations.py             # Gráficos personalizados
│   └── utils.py                      # Utilidades generales
│
├── 📁 powerbi/
│   ├── ecommerce_olist_dashboard.pbix
│   └── screenshots/                   # Capturas del dashboard
│
├── 📁 reports/
│   └── executive_summary.pdf
│
├── 📁 docs/
│   ├── methodology.md                # Metodología utilizada
│   └── insights.md                   # Insights encontrados
│
├── .gitignore
├── requirements.txt
└── README.md
```

---

## 🚀 Instalación y Setup

### 1. Clonar el repositorio

```bash
git clone https://github.com/devravehola/olist-ecommerce-analysis.git
cd olist-ecommerce-analysis
```

### 2. Crear entorno virtual

```bash
# Windows
python -m venv venv
venv\Scripts\activate

# Mac/Linux
python3 -m venv venv
source venv/bin/activate
```

### 3. Instalar dependencias

```bash
pip install -r requirements.txt
```

### 4. Descargar el dataset

1. Ve a [Kaggle - Brazilian E-Commerce Dataset](https://www.kaggle.com/datasets/olistbr/brazilian-ecommerce)
2. Descarga los archivos CSV
3. Colócalos en la carpeta `data/raw/`

### 5. Ejecutar notebooks

```bash
jupyter notebook
```

---

## 📊 Dataset

El dataset de **Olist** contiene información real de comercio electrónico brasileño entre 2016-2018.

### Archivos incluidos:
- `olist_customers_dataset.csv` - 99,441 clientes
- `olist_orders_dataset.csv` - 99,441 órdenes
- `olist_order_items_dataset.csv` - 112,650 items
- `olist_order_payments_dataset.csv` - 103,886 pagos
- `olist_order_reviews_dataset.csv` - 99,224 reviews
- `olist_products_dataset.csv` - 32,951 productos
- `olist_sellers_dataset.csv` - 3,095 vendedores
- `olist_geolocation_dataset.csv` - 1,000,163 ubicaciones
- `product_category_name_translation.csv` - 71 categorías

**Total de registros:** ~100K órdenes  
**Periodo:** 2016-2018  
**País:** Brasil 🇧🇷

---

## 📈 Análisis Realizados

### 1. Data Cleaning & Preparation
- Manejo de valores nulos
- Detección y tratamiento de outliers
- Conversión de tipos de datos
- Feature engineering

### 2. Exploratory Data Analysis (EDA)
- Estadísticas descriptivas
- Distribuciones de variables clave
- Análisis temporal
- Análisis geográfico

### 3. Sales Analysis
- Tendencias de ventas
- Análisis por categoría de producto
- Análisis por región
- Estacionalidad

### 4. Customer Segmentation (RFM)
- Recency, Frequency, Monetary
- Segmentación en grupos
- Customer Lifetime Value

### 5. Sentiment Analysis
- Análisis de texto de reviews
- Correlación review score vs ventas
- Factores que afectan satisfacción

### 6. Predictive Modeling
- Predicción de ventas
- Predicción de review score
- Time series forecasting

---

## 🎨 Dashboard Power BI

El dashboard interactivo incluye:

### 📊 Vista Ejecutiva
- KPIs principales (Revenue, Orders, AOV, etc.)
- Tendencias mensuales
- Comparativas año a año

### 🛍️ Vista de Productos
- Top productos por ventas
- Categorías más rentables
- Análisis de precio

### 👥 Vista de Clientes
- Segmentación RFM visual
- Mapa de clientes por región
- Análisis de retención

### 📦 Vista Operativa
- Tiempos de entrega
- Performance de vendedores
- Métodos de pago

---

## 🔍 Insights Principales

> Los insights específicos se irán documentando en `docs/insights.md` conforme avance el análisis.

---

## 🛠️ Tecnologías Utilizadas

- **Python 3.8+**
- **Pandas & NumPy** - Manipulación de datos
- **Matplotlib & Seaborn** - Visualización
- **Scikit-learn** - Machine Learning
- **Power BI** - Dashboards interactivos
- **Jupyter Notebook** - Análisis iterativo

---

## 👤 Autor

**Tu Nombre**
- GitHub: [@devravehola](https://github.com/devravehola)
- LinkedIn: [Tu LinkedIn]
- Email: tu-email@example.com

---

## 📝 Licencia

Este proyecto está bajo la Licencia MIT - ver el archivo [LICENSE](LICENSE) para más detalles.

---

## 🙏 Agradecimientos

- Dataset proporcionado por [Olist](https://olist.com/) en Kaggle
- Comunidad de Data Science en Kaggle

---

## 📅 Estado del Proyecto

🚧 **En desarrollo activo** - Última actualización: Febrero 2026

### Roadmap:
- [x] Setup inicial del proyecto
- [ ] Data cleaning completado
- [ ] EDA completado
- [ ] Análisis RFM completado
- [ ] Dashboard Power BI v1
- [ ] Modelos predictivos
- [ ] Documentación final