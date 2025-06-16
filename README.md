# dashboard-eda-callcenter
Resumen: 
El objetivo de este proyecto es aplicar técnicas de análisis exploratorio de datos y visualización mediante un dashboard que analice diferentes métricas relacionadas con un conjunto de datos de llamadas telefónicas de un call center

# 📊 Proyecto: Dashboard & Análisis de Datos 📊

**Nombre del archivo**: [Archivo en Google Sheets - Dashboard de Llamadas](https://docs.google.com/spreadsheets/d/1U2brCrCBTTKFwIvwh61Fc8zxVYA7TPijY60nUG2-VL8/edit?usp=sharing)

---

## 🧠 Objetivo del Proyecto

El objetivo de este proyecto es aplicar un EDA y la visualización mediante un dashboard con el que poder analizar métricas clave relacionadas con un conjunto de datos de contactos de una empresa de call center.

El **dashboard interactivo** permite interpretar visualmente información relacionada con distintas métricas (cantidad de contactos, duración media, contactos por día, motivo del contacto, ubicación, tanto del cliente (estado y ciudad), como de los diferentes call centers, tiempo de respuesta, etc...)

---

## 📂 Fuentes de Datos

- **Origen**: [Real World Fake Data - Kaggle](https://www.kaggle.com/datasets/mesumraza/real-world-fake-dataset-for-practice?resource=download )
- **Formato**: Google Sheets
- **Número de registros**: +2000
- **Número de columnas**: 12

---

## 🛠️ Proceso realizado

### 1. Limpieza y transformación de datos
- Creamos una copia del archivo original en otra hoja, para no perturbar los datos originales. A partir de aquí se hace referencia al trabajo realizado en dicha copia.
- Limpiamos registros que carecen de datos (hay 6 lineas que no tienen datos, unicamente el Id de llamada)
- Eliminamos la columna 'csat_score', satisfacción del cliente, ya que al hacer recuento de los que son válidos y los que no, (12268 con valor, frente a 20667 vacios), puede dar lugar a una gran distorsión, además existe una columna que hace una función similar - 'sentiment' (Opinión del cliente).
- A partir de la columna 'call_timestamp', como solo tenemos datos recogidos en Octubre de 2020, creamos:
  - Columna 'day', para mostrar el numero de día (1-31)
  - Columna 'week_day', para mostrar los días de la semana (lunes a domingo)

### 2. Análisis descriptivo
- **Distribución por días**: Se registran más picos de llamada en los días de mitad de semana (martes y miercoles)
- **Motivos de contacto**: El principal motivo de contacto fue *Billing Question*.
- **Canal de contacto**: El canal más utilizado fue **Call-Center** (teléfono), seguido por **Chatbot**.
- **Tiempo de respuesta**: Aproximadamente el 85% de las llamadas están dentro de los estandares de la empresa (Within SLA o Below SLA)
- **Duración media de las llamadas**: Apróximadamente unos 25 minutos
- **Sentimiento del cliente**:
  - Negativo o muy negativo: ~30%
  - Neutro: ~25%
  - Muy positivo: ~25%
  - Positivo: ~20%
- **Distribución geográfica**: Predominan llamadas de California, Florida y Texas, mientras que apenas hay de Wyioming y Vermont

### 3. Dashboard (Visualización e Interactividad)

- Se utilizaron **tablas dinámicas** y **gráficos** en Google Sheets
- Se añadieron **listas de validación como filtros** para permitir segmentación dinámica
- Gráficos principales:
  - Total de llamadas 
  - Duración media de llamada
  - Contactos por día
  - Recuento por estado
  - Tipo de canal y motivo de contacto
  - Sentimiento del cliente

## 📌 Informe Explicativo del analisis

- Las consultas sobre facturación (Billing Question) son las más comunes
- El telefono (call-center) sigue siendo el medio más utilizado para contactar, seguido pro el ChatBot, mostrando una oportunidad de automatizacion
- La satifacción de los clientes es un gran area de mejora (mayoria de clientes son detractores de la empresa, es decir no tienen sentimientos positivos).
- La duración de los contactos y su relacion con la satisfacción, puede sugerir que las los más  largos tienen que ver con clientes insatisfechos o con problemas que no se resuelven de manera ágil
- El tiempo de respuesta cumple en su mayoria con los estandares establecidos, lo cual es un punto positivo, aún así los que se contestan fuera de tiempo deberían investigarse
  
---

## 📁 Estructura del Repositorio

```
│
├── 📄 Call Center.csv ← Dataset original (Ver enlace más arriba en este documento)
│
├── 📄 Enlace-GoogleSheets.txt ← Enlace al documento compartido
│
└── README.md                   # Este archivo
