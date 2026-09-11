  <h1>📈 Análisis del INPC en México mediante Series de Tiempo (2003-2026)</h1>
  <p><i>Modelado predictivo de la inflación utilizando la metodología Box-Jenkins (ARIMA y SARIMA)</i></p>
</div>

<p align="center">
  <img src="https://img.shields.io/badge/Python-3776AB?style=for-the-badge&logo=python&logoColor=white" alt="Python">
  <img src="https://img.shields.io/badge/Pandas-150458?style=for-the-badge&logo=pandas&logoColor=white" alt="Pandas">
  <img src="https://img.shields.io/badge/SciPy-8CAAE6?style=for-the-badge&logo=scipy&logoColor=white" alt="SciPy">
  <img src="https://img.shields.io/badge/Statsmodels-000000?style=for-the-badge&logo=python&logoColor=white" alt="Statsmodels">
</p>

---

Este proyecto analiza la dinámica del **Índice Nacional de Precios al Consumidor (INPC)** en México, incluyendo sus componentes subyacente y no subyacente. El objetivo principal es identificar patrones temporales, evaluar el impacto de políticas económicas y generar pronósticos para el periodo 2020-2026.

## 👥 Equipo de Trabajo
* **Aranza Garcia Aguilar**
* **Fátima Landa Rodríguez**
* **Vanessa Lizeth Rivera Baez**
* **Nora Guadalupe Sanchez Montero**

📍 *Universidad Veracruzana, Licenciatura en Ingeniería en Ciencia de Datos.*

---

## 🗄️ Datos y Fuente
La información histórica fue obtenida de fuentes oficiales del **Instituto Nacional de Estadística y Geografía (INEGI)**.
* **Periodo de análisis:** Enero de 2003 a Marzo de 2026 (Frecuencia mensual).
* **Tamaño del dataset:** 843 observaciones estructuradas temporalmente.
* **Variables analizadas:** INPC General, Índice Subyacente e Índice No Subyacente.
* 📥 **Base de datos:** [conjunto_de_datos_inpc_mensual.csv](https://github.com/user-attachments/files/32082714/conjunto_de_datos_inpc_mensual.csv)<div align="center">



---

## 📊 Metodología y Visualizaciones

<div align="center">
 <img width="695" height="372" alt="Captura de pantalla 2026-09-10 194140" src="https://github.com/user-attachments/assets/dc54cc01-bbab-4452-87a2-7043b47729fb" />
  <br>
  <i>Comparación entre valores reales y pronosticados del INPC.</i>
</div>

### 1. Pruebas de Estacionariedad
Se aplicó la prueba **Dickey-Fuller Aumentada (ADF)**. Al confirmar la no estacionariedad de las series originales, se utilizaron transformaciones logarítmicas y diferenciación para estabilizar la media y varianza.

### 2. Modelado y Selección (Criterio AIC)
* **INPC General:** Modelo `ARIMA(2,1,1)`
* **Índice Subyacente:** Modelo `SARIMA(2,1,3)(0,0,1,12)`
* **Índice No Subyacente:** Modelo `SARIMA(2,1,2)(2,0,2,12)`

### 3. Validación y Pronósticos
Análisis de residuos mediante histogramas, gráficos QQ-Plot y correlogramas para comprobar normalidad e independencia. Proyecciones comparadas contra valores reales utilizando métricas **MAE** y **RMSE**.

---

## 📌 Hallazgos Principales y Conclusiones
- 🟢 **Estabilidad:** El **Índice Subyacente** presentó el comportamiento más estable a lo largo del tiempo, facilitando un modelo predictivo con menor margen de incertidumbre.
- 🔴 **Volatilidad:** El **Índice No Subyacente** mostró fluctuaciones bruscas, fuertemente asociado a variaciones externas en precios energéticos y productos agropecuarios.
- 📉 **Impacto de Políticas:** Los modelos capturaron adecuadamente la tendencia de crecimiento frente a eventos como la Crisis de 2008 y la pandemia de COVID-19, reflejando el impacto de las tasas de interés del Banco de México.
- ⚠️ **Limitaciones:** En periodos de alta volatilidad atípica (como 2021-2023), los residuos del modelo general muestran desviaciones de la normalidad debido a choques económicos externos impredecibles.

---

## 🚀 Cómo ejecutar el proyecto

Para reproducir este análisis en tu máquina local:

1. Clona este repositorio:
   ```bash
   git clone [https://github.com/tu-usuario/An-lisis-del-comportamiento-del-ndice-Nacional-de-Precios-al-Consumidor-.git](https://github.com/tu-usuario/An-lisis-del-comportamiento-del-ndice-Nacional-de-Precios-al-Consumidor-.git)


[PROYECTO SERIES DE TIEMPO.pdf](https://github.com/user-attachments/files/32082445/PROYECTO.SERIES.DE.TIEMPO.pdf)
