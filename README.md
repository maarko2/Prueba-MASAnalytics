# Mini-Demo Técnica: Análisis de Ventas Estacionales

## Descripción
Esta mini-demo técnica muestra cómo procesar y visualizar datos de ventas estacionales para apoyar decisiones de negocio.  
El caso ficticio simula cómo un negocio puede anticipar picos y caídas en ventas durante el año, utilizando datos de un CSV público de Kaggle.

---

## Contenido del repositorio

- `notebook/Demo Mas Analytics.dbc`  
  Notebook de Databricks con todo el flujo: carga de datos, transformación con PySpark y exportación.

- `data/Grocery_Inventory_and_Sales_Dataset.csv`  
  CSV con los datos de ventas utilizado en la demo.

- `README.md`  
  Este archivo con instrucciones de uso.

- `Dashboard-MAS-Analytics.pbix`  
  Archivo para PowerBI

---

## Prerrequisitos

- Ingresar a Databricks  
- Subir el archivo CSV a Databricks (DBFS) antes de ejecutar el notebook.
- Subir el archivo .dbc

---

## Instrucciones para ejecutar la demo

1. **Importar Notebook**
   - En Databricks: Workspace → Import → File → selecciona `Demo MAS Analytics.dbc`.
   - Haz clic en Import.

2. **Subir CSV**
   - En Databricks: Data → Create Table → Upload File → selecciona `Grocery_Inventory_and_Sales_Dataset.csv`.
   - Nota: ajustar la ruta en el notebook si es necesario:
     ```python
     df = spark.read.csv("/FileStore/tables/Grocery_Inventory_and_Sales_Dataset.csv", header=True, inferSchema=True)
     display(df)
     ```

3. **Ejecutar Notebook**
   - Ejecuta celda por celda.
   - Transformaciones: agregación de ventas por mes y año.
   - Exportación de resultados a CSV o visualización en Power BI.

4. **Visualizar Resultados**
   - Abrir Power BI.
   - Cargar los CSV generados desde el notebook.
   - Crear gráficos de ventas por mes y año.

---

## Valor de negocio
- Permite identificar meses con baja o alta demanda.  
- Optimiza inventario y planificación de marketing.  
- Ayuda a anticipar decisiones basadas en datos reales.
