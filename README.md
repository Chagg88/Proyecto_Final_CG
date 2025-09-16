# 📊 Análisis de Ventas y Perfil de Clientes en Tienda de Ropa Deportiva

## 📖 Descripción del Proyecto
Este proyecto realiza un análisis exhaustivo de los productos vendidos y del perfil de los clientes de una tienda especializada en ropa deportiva. Se busca estudiar el comportamiento de ventas, evaluar características de productos, y segmentar clientes para identificar patrones de consumo y optimizar estrategias comerciales. El análisis se basa en técnicas de análisis exploratorio, estadístico y visualización de datos.

---

## 🗂 Estructura del Proyecto

```

Informe/
├── Informe Proyecto.pdf
Notebooks/
├── 01_EDA_preliminar_SportStoreSales.ipynb
├── 02_Creacion_Columnas_vf.ipynb
├── 03_Analisis_col_cat_sport_vf.ipynb
├── 04_Analisis_col_num_sport_vf.ipynb
PowerBi_Dashboard/
├── Proyecto_Final_vf.pbix
Raw_Data/
├── Product_Catalog.csv
├── Sales_2023_2024.csv
Transformed_Data/
├── Merge_Data_Profit_VF.csv
README.md

```

---

## 🛠 Instalación y Requisitos

Para correr los cuadernos y realizar el análisis, es necesario contar con Python 3.8 o superior y las siguientes librerías:

- pandas  
- numpy  
- matplotlib  
- seaborn  

Además, para la visualización interactiva se utilizó Power BI.

---

## 📊 Resultados y Conclusiones

- Ventas netas totales de 99,7 millones de euros con un margen de beneficio medio del 30,4% en 2023-2024.
- Incremento del 17,7% en ventas netas en 2024 respecto a 2023, motivado por un aumento en el número de operaciones.
- Distribución uniforme de ventas en 8 mercados internacionales, sin país dominante.
- Perfil de clientes balanceado entre géneros y membresías.
- Rendimiento equilibrado entre categorías (Clothing, Accessories, Equipment, Footwear).
- Top 5 productos más vendidos: Running shoes, Boots, Pants, T-shirts, Sneakers.

---

### 🔠 Columnas categóricas

Se realizó un análisis de las columnas categóricas:  
`job`, `marital`, `education`, `contact`, `poutcome`, `y`

- `job`: 11 valores únicos  
  Casi el 50% de los datos se concentran en:
  - `admin` (25,5%)
  - `blue-collar` (22,6%)

- `marital`: 3 valores únicos  
  - 60,6% `married`  
  - 28,2% `single`  
  - 11,2% `divorced`

- `education`: 7 valores únicos  
  - 30,9% `university degree`  
  - 24,1% `high-school`  
  - Requiere clarificación de las categorías `basic (9y, 6y, 4y)` para posible agrupación.

- `contact`: 2 valores únicos  
  - 63,7% `cellular`  
  - 36,3% `telephone`

- `poutcome`: 3 valores únicos  
  - 86,3% no tenían campaña previa  
  - 10,4% campaña fallida  
  - 3,3% campaña exitosa

- `y`: 88,7% de los clientes **no** han suscrito productos/servicios

---

### 📈 Columnas numéricas

Se han identificado **outliers** en las columnas:

- `age`
- `default`
- `duration`
- `campaign`
- `previous`
- `euribor`

Sería interesante comentar con el cliente si se trata de valores erróneos o reales que hay que analizar de manera diferente.

> Se ha decidido sustituir todos los valores nulos por `"unknown"`.

Este análisis exploratorio ha permitido entender la estructura, calidad y composición de los datos, sentando una base sólida para las etapas posteriores del análisis.

> La colaboración con el cliente será clave para resolver ciertas ambigüedades y tomar decisiones adecuadas para la preparación de datos.

---


  ---

  ## 🔄 Próximos Pasos

- Refinar el análisis con más datos y variables adicionales.
- Implementar análisis predictivo y modelos de recomendación.
- Mejorar y expandir el dashboard interactivo con Power BI.

  ---

  ## 🤝 Contribuciones

Las contribuciones son bienvenidas.

 ---

## ✒ Autores y Agradecimientos

- Christian Garcini - [@Chagg88](https://github.com/Chagg88)
