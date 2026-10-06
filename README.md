# 📊 Dashboard & Análisis de Datos — Call Center

Análisis exploratorio y dashboard de datos de un call center para identificar patrones de contacto, tiempos de respuesta, motivos y sentimiento del cliente.

## 🎯 Objetivo

El objetivo de este proyecto es aplicar técnicas de **análisis exploratorio de datos (EDA)** y visualización para analizar diferentes métricas relacionadas con los contactos de un servicio de atención al cliente.

El dashboard permite explorar aspectos como:

- Volumen de llamadas y distribución temporal.
- Duración media de los contactos.
- Motivos de contacto.
- Canales utilizados por los clientes.
- Tiempo de respuesta y cumplimiento del SLA.
- Distribución geográfica de los contactos.
- Sentimiento del cliente.

## 📊 Dashboard

El análisis y el dashboard fueron desarrollados utilizando **Google Sheets**, mediante tablas dinámicas, gráficos y filtros interactivos.

**[Ver Dashboard de Llamadas en Google Sheets](https://docs.google.com/spreadsheets/d/1U2brCrCBTTKFwIvwh61Fc8zxVYA7TPijY60nUG2-VL8/edit?usp=sharing)**

El dashboard permite segmentar la información y analizar diferentes métricas de forma dinámica.

## 📂 Datos

Los datos proceden del dataset **Real World Fake Data**, disponible en Kaggle.

- **Fuente:** [Real World Fake Data - Kaggle](https://www.kaggle.com/datasets/mesumraza/real-world-fake-dataset-for-practice?resource=download)
- **Formato de trabajo:** Google Sheets
- **Registros:** +2.000
- **Columnas originales:** 12
- **Periodo analizado:** octubre de 2020

## 🔄 Proceso de análisis

El proyecto se desarrolló en varias etapas.

### 1. Limpieza y transformación

Se realizó una copia de los datos originales para trabajar sobre ella sin modificar la fuente inicial.

Durante esta fase:

- Se eliminaron 6 registros que únicamente contenían el identificador de llamada y no aportaban información adicional.
- Se eliminó la columna `csat_score` debido al elevado número de valores vacíos. Además, el dataset dispone de la variable `sentiment`, que permite analizar la percepción del cliente desde otra perspectiva.
- A partir de `call_timestamp` se crearon nuevas variables para facilitar el análisis temporal:
  - `day`: día del mes.
  - `week_day`: día de la semana.

### 2. Análisis exploratorio

A partir de los datos preparados se analizaron diferentes dimensiones del servicio.

#### Distribución temporal

Se observan mayores volúmenes de llamadas durante determinados días de la semana, destacando especialmente martes y miércoles.

#### Motivos de contacto

El motivo de contacto más frecuente es **Billing Question**, relacionado con consultas de facturación.

#### Canal de contacto

El **Call Center** es el canal más utilizado, seguido del **Chatbot**.

Este comportamiento permite identificar el peso que continúa teniendo la atención telefónica y, al mismo tiempo, el papel de los canales automatizados.

#### Tiempo de respuesta

Aproximadamente el **85 % de las llamadas** se encuentran dentro de los estándares establecidos por la empresa, clasificadas como `Within SLA` o `Below SLA`.

Los contactos que quedan fuera de estos estándares representan un punto de interés para un análisis posterior.

#### Duración de las llamadas

La duración media de los contactos se sitúa aproximadamente en **25 minutos**.

#### Sentimiento del cliente

La distribución observada es aproximadamente:

- Negativo o muy negativo: ~30 %
- Neutro: ~25 %
- Muy positivo: ~25 %
- Positivo: ~20 %

El sentimiento del cliente constituye uno de los principales puntos de interés del análisis.

#### Distribución geográfica

Los estados con mayor volumen de contactos son **California, Florida y Texas**, mientras que estados como **Wyoming y Vermont** presentan una representación mucho menor.

## 📈 Principales conclusiones

El análisis permite identificar varios patrones relevantes:

- Las consultas relacionadas con **facturación** son el principal motivo de contacto.
- El **teléfono** continúa siendo el canal más utilizado, seguido del **Chatbot**, lo que muestra la importancia de analizar la evolución y posible automatización de determinados tipos de consultas.
- La distribución del **sentimiento del cliente** muestra un margen importante de mejora en la experiencia de atención.
- La **duración de los contactos** puede ser una variable interesante para estudiar junto con el sentimiento y el motivo de contacto, aunque este proyecto no establece una relación causal entre estas variables.
- Aunque la mayoría de los contactos cumplen los estándares de tiempo de respuesta, los casos fuera de SLA representan una oportunidad para profundizar en las causas y detectar posibles problemas operativos.

## 🛠️ Herramientas utilizadas

- Google Sheets
- Tablas dinámicas
- Gráficos
- Filtros y listas de validación
- Análisis exploratorio de datos (EDA)

## 📊 Métricas y visualizaciones

El dashboard incluye diferentes elementos para facilitar la exploración de los datos:

- Total de llamadas.
- Duración media de las llamadas.
- Contactos por día.
- Distribución por estado.
- Canal de contacto.
- Motivo de contacto.
- Sentimiento del cliente.
- Tiempo de respuesta y cumplimiento del SLA.

## 📁 Estructura del repositorio

    ├── 📄 Call Center.csv
    ├── 📄 Enlace-GoogleSheets.txt
    └── 📄 README.md

### `Call Center.csv`

Dataset original utilizado como fuente para el análisis.

### `Enlace-GoogleSheets.txt`

Archivo que contiene el enlace al documento de Google Sheets donde se encuentra el análisis y dashboard.

## ℹ️ Contexto del proyecto

Proyecto realizado como ejercicio práctico de **análisis exploratorio de datos y visualización**, centrado en la interpretación de información operativa y de experiencia del cliente.

El objetivo no es únicamente representar los datos, sino utilizarlos para identificar patrones y posibles áreas de mejora dentro del servicio de atención.
