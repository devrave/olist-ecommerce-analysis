# 📊 Data Directory

Esta carpeta contiene los datos del proyecto.

## 📁 Estructura

```
data/
├── raw/          # Datos originales sin modificar
└── processed/    # Datos procesados y limpios
```

---

## 📥 raw/

**Descripción:** Datos originales descargados de Kaggle (Olist Dataset)

**Archivos esperados:**
- `olist_customers_dataset.csv`
- `olist_geolocation_dataset.csv`
- `olist_order_items_dataset.csv`
- `olist_order_payments_dataset.csv`
- `olist_order_reviews_dataset.csv`
- `olist_orders_dataset.csv`
- `olist_products_dataset.csv`
- `olist_sellers_dataset.csv`
- `product_category_name_translation.csv`

**Fuente:** [Kaggle - Brazilian E-Commerce Public Dataset by Olist](https://www.kaggle.com/datasets/olistbr/brazilian-ecommerce)

⚠️ **Nota:** Los archivos CSV NO se suben a GitHub (están en `.gitignore`) por su tamaño.

---

## 📤 processed/

**Descripción:** Datos procesados generados por los notebooks de limpieza y transformación.

**Archivos generados:**
- `orders_clean.csv` - Órdenes limpias
- `customers_segmented.csv` - Clientes con segmentación RFM
- `sales_aggregated.csv` - Ventas agregadas para Power BI
- `master_dataset.parquet` - Dataset maestro unificado

⚠️ **Nota:** Estos archivos también están en `.gitignore`

---

## 🔗 Relaciones entre tablas

```
orders (tabla principal)
├── customer_id → customers
├── order_id → order_items
│   ├── product_id → products
│   └── seller_id → sellers
├── order_id → order_payments
└── order_id → order_reviews

customers
└── customer_zip_code_prefix → geolocation

sellers
└── seller_zip_code_prefix → geolocation
```

---

## 📖 Diccionario de Datos

### **olist_orders_dataset.csv**
| Campo | Tipo | Descripción |
|-------|------|-------------|
| order_id | string | ID único de la orden |
| customer_id | string | ID del cliente |
| order_status | string | Estado de la orden |
| order_purchase_timestamp | datetime | Fecha de compra |
| order_approved_at | datetime | Fecha de aprobación |
| order_delivered_carrier_date | datetime | Fecha entrega al carrier |
| order_delivered_customer_date | datetime | Fecha entrega al cliente |
| order_estimated_delivery_date | datetime | Fecha estimada de entrega |

### **olist_order_items_dataset.csv**
| Campo | Tipo | Descripción |
|-------|------|-------------|
| order_id | string | ID de la orden |
| order_item_id | int | Número secuencial del item |
| product_id | string | ID del producto |
| seller_id | string | ID del vendedor |
| shipping_limit_date | datetime | Límite de envío |
| price | float | Precio del producto |
| freight_value | float | Costo de envío |

### **olist_customers_dataset.csv**
| Campo | Tipo | Descripción |
|-------|------|-------------|
| customer_id | string | ID único del cliente |
| customer_unique_id | string | ID único real |
| customer_zip_code_prefix | string | Código postal |
| customer_city | string | Ciudad |
| customer_state | string | Estado |

### **olist_products_dataset.csv**
| Campo | Tipo | Descripción |
|-------|------|-------------|
| product_id | string | ID único del producto |
| product_category_name | string | Categoría (en portugués) |
| product_name_lenght | int | Longitud del nombre |
| product_description_lenght | int | Longitud de descripción |
| product_photos_qty | int | Cantidad de fotos |
| product_weight_g | int | Peso en gramos |
| product_length_cm | int | Largo en cm |
| product_height_cm | int | Alto en cm |
| product_width_cm | int | Ancho en cm |

### **olist_sellers_dataset.csv**
| Campo | Tipo | Descripción |
|-------|------|-------------|
| seller_id | string | ID único del vendedor |
| seller_zip_code_prefix | string | Código postal |
| seller_city | string | Ciudad |
| seller_state | string | Estado |

### **olist_order_payments_dataset.csv**
| Campo | Tipo | Descripción |
|-------|------|-------------|
| order_id | string | ID de la orden |
| payment_sequential | int | Secuencia de pago |
| payment_type | string | Tipo de pago |
| payment_installments | int | Cuotas |
| payment_value | float | Valor del pago |

### **olist_order_reviews_dataset.csv**
| Campo | Tipo | Descripción |
|-------|------|-------------|
| review_id | string | ID único del review |
| order_id | string | ID de la orden |
| review_score | int | Puntuación (1-5) |
| review_comment_title | string | Título del comentario |
| review_comment_message | string | Mensaje del comentario |
| review_creation_date | datetime | Fecha de creación |
| review_answer_timestamp | datetime | Fecha de respuesta |

---

## 📊 Estadísticas del Dataset

- **Periodo:** Septiembre 2016 - Agosto 2018
- **Órdenes:** ~100,000
- **Productos:** ~33,000
- **Vendedores:** ~3,000
- **Clientes:** ~99,000
- **Categorías:** 73

---

## 🔄 Proceso de Datos

1. **Raw Data** → Descarga desde Kaggle
2. **Data Cleaning** → `01_data_cleaning.ipynb`
3. **Feature Engineering** → `02_eda.ipynb`
4. **Processed Data** → Guardado en `processed/`
5. **Power BI** → Importa datos de `processed/`