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

Para correr los cuadernos y realizar el análisis, es necesario contar con Python 3.12 o superior y las siguientes librerías:

- pandas  
- numpy  
- matplotlib  
- seaborn  

Además, para la visualización interactiva se utilizó Power BI.

---

## 🗃 Raw Data

El cliente ha proporcionado dos conjuntos de datos que constituyen la base para este análisis:

- Dataset de ventas (`Sales_2023_2024.csv`): contiene los registros de transacciones comerciales con detalles y perfil de los clientes.
- Dataset de catálogo de productos (`Product_catalog.xlsx`): información descriptiva y variables clave para el análisis de productos.

Ambos archivos están vinculados por la variable común `Product_ID`, facilitando la integración entre datos transaccionales y descripción detallada de productos.

### Detalle de columnas del dataset de ventas

- `Sale_ID`: Identificador único de cada registro de venta.
- `Product_ID`: Código del producto vendido.
- `Store_Country`: País donde se realizó la venta.
- `Quantity_Sold`: Cantidad vendida.
- `Discount_percent`: Porcentaje de descuento aplicado.
- `Sale_Date`: Fecha de la venta.
- `Payment_Method`: Método de pago del cliente.
- `Customer_Age`: Edad del cliente.
- `Customer_Gender`: Género del cliente.
- `Membership`: Estado de membresía del cliente.

### Detalle de columnas del catálogo de productos

- `Product_ID`: Identificador único.
- `Product_Name`: Nombre comercial del producto.
- `Category`: Departamento de venta al que pertenece.
- `Sale_Price_EUR`: Precio final de venta (sin descuento).
- `Cost_Price_EUR`: Precio de coste para la empresa.
- `Stock`: Stock disponible.
- `Country_Origin`: País de fabricación.
- `Brand`: Marca del producto.
- `Color`: Color principal.
- `Size`: Talla o medida relevante.
- `Gender`: Género objetivo del producto.

---

## ⚙️ Metodología

El análisis se inició con la exploración preliminar de los datos (EDA) usando Python y la librería Pandas en Visual Studio Code. Se validó la calidad de los datos, confirmando ausencia de valores nulos y duplicados, y se estandarizaron los formatos numéricos y de fecha.

Los datasets se integraron utilizando `Product_ID` como clave común, y se crearon variables derivadas para enriquecer el análisis:

- `Gross_Sales`: Ingreso bruto (Quantity_Sold * Sale_Price_EUR).
- `Total_Discount`: Descuento total aplicado.
- `Net_Sales`: Ventas netas después del descuento.
- `Total_Cost`: Coste total asociado.
- `Total_Profit_EUR`: Ganancia total (Net_Sales – Total_Cost).
- `Profit_Percentage`: Margen de beneficio (% sobre ventas netas).

El dataset final fue exportado para su análisis avanzado y visualización en Power BI, aplicando análisis descriptivos diferenciados para variables categóricas y numéricas para identificar patrones relevantes.

---

## 📊 Resultados y Conclusiones

- Ventas netas totales de 99,7 millones de euros con un margen de beneficio medio del 30,4% en 2023-2024.
- Incremento del 17,7% en ventas netas en 2024 respecto a 2023, motivado por un aumento en el número de operaciones (41.449 transacciones en 2024 y 35.129 en 2023).
- Distribución uniforme de ventas en 8 mercados internacionales, sin país dominante.
- Perfil de clientes balanceado entre géneros y membresías.
- Rendimiento equilibrado entre categorías (Clothing, Accessories, Equipment, Footwear).
- Top 5 productos más vendidos: Running shoes, Boots, Pants, T-shirts, Sneakers.

---

### 🗃️ Estructura de los Datos

El conjunto de datos de ventas contiene un total de 76.578 registros con 9 columnas que describen cada transacción, mientras que el catálogo de productos aporta 1.716 registros con 11 columnas descriptivas. Tras la unión mediante la variable común `Product_ID`, se obtuvo un dataset final con 76.578 filas y 20 columnas. Para facilitar el análisis y la visualización, se añadieron seis columnas derivadas: `Gross_Sales`, `Total_Discount`, `Net_Sales`, `Total_Cost`, `Total_Profit_EUR` y `Profit_Percent`, ampliando el conjunto final a un total de 26 columnas.

### ✔️ Calidad y Preparación de Datos

Se verificó que el conjunto no contenía valores nulos ni registros duplicados. Se realizó la transformación necesaria para garantizar la correcta interpretación de los datos numéricos y de fechas, estandarizando formatos y asegurando la integridad para un análisis fiable.


### 🔠 Columnas categóricas

Se realizó un análisis de las columnas categóricas:  
`Sale_ID`, `Product_ID`, `Store_Country`, `Payment_Method`, `Customer_Gender`, `Memebership`, `Product_Name`, `Category`, `Country_Origin`, `Brand`, `Color`, `Size`, `Gender`

- `Sale_ID`: 76.578 valores únicos  

- `Product_ID`: 1.716 valores únicos y el dato más repetido es S001148 con una frecuencia de 67 veces  

- `Store_Country`: 8 valores únicos y el dato más repetido es Spain con una frecuencia de 9.673 veces (12,6%)  

- `Payment_Method`:  4 valores únicos y el dato más repetido es Paypal con una frecuencia de 19.248 veces (25,1%)  

- `Customer_GendeR`: 3 valores únicos y el dato más repetido es female con una frecuencia de 25.669 veces (33,5%)  

- `Memebership`: 2 valores únicos y el dato más repetido es Yes con una frecuencia de 38.429 veces (50,2%)

- `Product_Name`: 25 valores únicos y el dato más repetido es Running shoes con una frecuencia de 4.826 veces (6,3%)

- `Category`: 4 valores únicos y el dato más repetido es Accessories con una frecuencia de 19.428 veces (25,4%)

- `Country_Origin`: 8 valores únicos y el dato más repetido es México con una frecuencia de 10.465 veces (13,7%) 

- `Brand`: 5 valores únicos y el dato más repetido es Reebok con una frecuencia de 16.292 veces (21,3%)

- `Color`: 6 valores únicos y el dato más repetido es red con una frecuencia de 14.027 veces (18,3%)

- `Size`: 4 valores únicos y el dato más repetido es L con una frecuencia de 20.095 veces (26,2%)

- `Gender`: 2 valores únicos y el dato más repetido es Male con una frecuencia de 40.156 veces (52,4%)

---

### 📈 Columnas numéricas

Se han analizado las siguientes columnas numéricas:

- `Quantity_Sold`
- `Discount_percent`
- `Custoomer_Age`
- `Sale_Price_EUR`
- `Cost_Price_EUR`
- `Stock`
- `Gross_Sale`
- `Total_Discount`
- `Net_Sales`
- `Total_Cost`
- `Total_Profit_EUR`
- `Profit_Percent`

Mediante histogramas y boxplots se exploraron la distribución de las principales variables numéricas, evidenciando la variabilidad y tendencias en cantidad vendida, precios, descuentos, costos y beneficios. 

No se observan outliers que puedan estar afectando las estadísticas básicas de nuestros datos.

En total `Total_Profit_EUR` Se ha identificado un valor mínimo, lo que sugiere que hay alguna venta que esta generando pérdidas. El valor es de -21,75 euros, no es releventa pero resulta interesante entender con el cliente que fue lo que ocasionó esto. 

---


  ---

  ## 🔄 Próximos Pasos

- Entendder con el cliente cuál fue el factor que incremento el número de transacciones en el año
- Definir con el cliente un rango para establecer una especie de clusters que permitan tener un mejor entendimiento del perfil de clientes de la tienda  
- Refinar el análisis con más datos y variables adicionales.
- Implementar análisis predictivo y modelos de recomendación.

  ---

  ## 🤝 Contribuciones

Las contribuciones son bienvenidas.

 ---

## 👤 Autor

- GitHub: [@Chagg88](https://github.com/Chagg88)  
- Email: [cgarcini_m88@hotmail.com](mailto:cgarcini_m88@hotmail.com)
