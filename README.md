# conectatel-analisys
ConnectaTel – Uso y Segmentación de Clientes · Sprint 7

Este repositorio contiene el análisis realizado durante el Sprint 7 del caso ConnectaTel,
empresa de telecomunicaciones con operaciones en México y Colombia.

Se trabajó con tres datasets que totalizan más de 44,000 registros entre usuarios,
eventos de uso y catálogo de planes. Los datos incluyen valores faltantes, centinelas,
outliers y problemas de calidad diseñados para simular datos reales del sector telecom.

---

## 📂 Contenido del repositorio

- `notebooks/ConnectaTel_analysis.ipynb`
  → Notebook principal con carga, limpieza, EDA, distribuciones, outliers, segmentación e insight ejecutivo.

- `datasets/`
  - `plans.csv` → Catálogo de planes: precios, minutos, GB incluidos y costos por excedente
  - `users_latam.csv` → Información de 4,000 clientes: edad, ciudad, plan, fechas de registro y churn
  - `usage.csv` → 40,000 eventos de uso: llamadas (duración) y mensajes (longitud)

---

## ▶️ Cómo abrir el notebook en Google Colab

Haz clic en el siguiente botón:
[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/drive/15OjSjj7DvHpi009ZPGjXhCd6L4Ercywq?usp=sharing)
O:
1. Abre el archivo `.ipynb` en GitHub
2. Haz clic en **Open in Colab**

---

## 📘 Cómo reproducir el análisis

1. Abre `notebooks/ConnectaTel_analysis.ipynb` en Google Colab
2. Monta tu Google Drive si los datasets están almacenados ahí:
```python
# cargar archivos
# En JupyterNotebooks - - - - - - - - - - - - - - - - - - - - -
#plans = pd.read_csv('/datasets/plans.csv')
#users = pd.read_csv('/datasets/users_latam.csv')
#usage = pd.read_csv('/datasets/usage.csv')
# - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - -

# 1. Montar Google Drive (solo se ejecuta una vez por sesión)
from google.colab import drive
drive.mount('/content/drive')

# 2. Leer los CSV con la ruta correcta
import pandas as pd
plans = pd.read_csv('/content/drive/MyDrive/Colab Notebooks/datasets/plans.csv')
users = pd.read_csv('/content/drive/MyDrive/Colab Notebooks/datasets/users_latam.csv')
usage = pd.read_csv('/content/drive/MyDrive/Colab Notebooks/datasets/usage.csv')
```
3. Ejecuta las celdas en orden — el notebook sigue un flujo secuencial de 8 pasos
4. Los datasets deben estar en la ruta `/datasets/` o en la carpeta de Drive configurada

---

## 🧠 Objetivo del análisis

- Detectar y documentar problemas de calidad de datos (nulos, centinelas, fechas fuera de rango)
- Construir un pipeline de limpieza reproducible y trazable
- Construir un perfil estadístico de uso por cliente (llamadas, mensajes, minutos)
- Detectar outliers y comportamientos atípicos mediante métodos estadísticos (IQR) y visuales
- Crear segmentos de clientes por edad y nivel de uso
- Generar insights y recomendaciones comerciales para el equipo de ConnectaTel

---

## 💡 Preguntas de negocio respondidas

- ¿Qué segmentos muestran mayor o menor uso de llamadas y mensajes?
- ¿Qué usuarios presentan valores atípicos que puedan indicar comportamientos inusuales?
- ¿Cómo varía el uso según la edad y el tipo de plan contratado?
- ¿Qué patrones ayudan a diseñar mejores planes y optimizar la oferta comercial?

---

## 🔄 Flujo del proyecto

| Paso | Acción | Resultado |
|------|--------|-----------|
| 1 | Cargar y explorar los 3 datasets | Visión clara de estructura y tipos de datos |
| 2 | Identificar problemas de calidad | Lista priorizada de inconsistencias |
| 3 | Limpieza básica | Datos consistentes listos para análisis |
| 4 | Summary statistics | Medidas clave por variable y segmento |
| 5 | Visualización y outliers | Histogramas, boxplots, detección por IQR |
| 6 | Segmentación | Grupos por edad y nivel de uso |
| 7 | Insight ejecutivo | Conclusiones y recomendaciones accionables |
| 8 | Publicación | Notebook + README en GitHub |

---

## 🛠️ Herramientas utilizadas

- Python 3.9
- pandas · numpy · seaborn · matplotlib
- Jupyter Notebook / Google Colab

---

## 👤 Autor

`MARISOL MARTINEZ PULGARIN`
Sprint 7 · Análisis de Datos · TripleTen LATAM
