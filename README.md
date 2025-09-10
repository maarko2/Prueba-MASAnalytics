# Mini-Demo Técnica: Análisis de Ventas Estacionales

## Descripción
Esta mini-demo técnica muestra cómo procesar y visualizar datos de ventas estacionales para apoyar decisiones de negocio.  
El caso ficticio simula cómo un negocio puede anticipar picos y caídas en ventas durante el año, utilizando datos de un CSV público de Kaggle.

---

## Contenido del repositorio

- `notebook/mini_demo_ventas.dbc`  
  Notebook de Databricks con todo el flujo: carga de datos, transformación con PySpark y exportación.

- `data/grocery_sales.csv`  
  CSV con los datos de ventas utilizado en la demo.

- `README.md`  
  Este archivo con instrucciones de uso.

- `PPT_mini_demo.pdf`  
  Presentación orientada a un cliente no técnico, mostrando problemática y resultados.

---

## Prerrequisitos

- Cuenta gratuita en [Databricks Community Edition](https://community.cloud.databricks.com/).  
- Tener descargado este repositorio en tu equipo.  
- Subir el archivo CSV a Databricks (DBFS) antes de ejecutar el notebook.

---

## Instrucciones para ejecutar la demo

1. **Importar Notebook**
   - En Databricks: Workspace → Import → File → selecciona `mini_demo_ventas.dbc`.
   - Haz clic en Import.

2. **Subir CSV**
   - En Databricks: Data → Create Table → Upload File → selecciona `grocery_sales.csv`.
   - Nota: ajustar la ruta en el notebook si es necesario:
     ```python
     df = spark.read.csv("/FileStore/tables/grocery_sales.csv", header=True, inferSchema=True)
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

---

## Contacto
Para cualquier consulta, revisar los comentarios en el notebook o contactar al autor.
