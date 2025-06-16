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

### 2. EDA y dashboard
Mediante los distintos filtros que se aplican en el **dashboard dinamico** se pueden obtener diferentes insights tanto a nivel numerico como visual mediante las gráficas:

- Recuento de llamadas, que con los distintos gráficos y filtros se pueden especificar
- Duración promedio de la llamada
- Llamadas por estado y ciudad
- Motivos de llamada
- Llamadas diarias
- Forma de contacto (dentro de llamadas se incluye cualquier contacto con los call center)
- Tiempo de respuesta (para ver si se cumplen los estandares de la empresa)
- Motivo de la llamada

Los **gráficos** tienen formato dinamico gracias a las **listas da validación**, que actuan como filtros.

## 📌 Conclusiones

- La media de contactos se mantiene a lo largo del mes entre 1000 y 1250, con la excepción del último día del mes
- El motivo más comun de los contactos es sobre facturación (Billing question)
- Los estados de California y Texas son los que más han contactado, frente a Wyioming y Vermont que son los que menos
- La mayoría de llamadas se han contestado dentro del plazo establecido por la empresa (Within SLA o Bellow SLA).
- El medio más popular de contacto ha sido teléfono (call center).
  
---

## 📁 Estructura del Repositorio
```
│
├── 📄 Call Center.csv ← Dataset original (Ver enlace más arriba en este documento)
│
├── 📄 Enlace-GoogleSheets.txt← Contiene el enlace a la hoja compartida
│
└── README.md                   # Este archivo
