# Análisis de ventas en centros comerciales con Python

Análisis de 99.457 transacciones registradas en centros comerciales de Estambul entre el **1 de enero de 2021 y el 8 de marzo de 2023**.

Mediante Python y Pandas se estudian los ingresos por centro comercial y categoría, el volumen de ventas y la actividad comercial por fechas.

## Objetivos

- Calcular la facturación total e identificar el centro comercial con mayores ingresos.
- Analizar las categorías con mayor volumen de unidades vendidas y su contribución a la facturación.
- Identificar las fechas y los días de la semana con mayor actividad comercial.
- Analizar el volumen medio de compra y las transacciones de mayor importe.

## Datos

Las principales variables utilizadas son:

| Variable | Descripción |
|---|---|
| `invoice_no` | Identificador de la factura |
| `customer_id` | Identificador del cliente |
| `category` | Categoría del producto |
| `quantity` | Unidades vendidas |
| `price` | Precio unitario |
| `invoice_date` | Fecha de la transacción |
| `shopping_mall` | Centro comercial |

Para calcular la facturación se multiplica el precio unitario por la cantidad vendida (`quantity * price`). Los importes se expresan en **liras turcas (TRY)**.

El archivo utilizado procede de una actividad formativa. Como referencia para obtener los datos originales puede consultarse [Customer Shopping Dataset — Kaggle](https://www.kaggle.com/datasets/mehmettahiraslan/customer-shopping-dataset), publicado por Mehmet Tahir Aslan.

## Resultados principales

| Indicador | Resultado |
|---|---|
| Facturación total | 1.490,92 millones de TRY |
| Centro comercial con mayor facturación | Mall of Istanbul |
| Categoría con más unidades vendidas | Clothing (ropa) |
| Participación de Clothing en la facturación | 34,50 % |
| Promedio de unidades por transacción | 3,00 |
| Día con mayor número de transacciones | 24/11/2021 |
| Factura de mayor importe | I311640 — 49.998 TRY |

### Conclusiones

La ropa es la categoría con mayor peso en la facturación (34,50 %). Junto con cosmética y alimentación y bebidas, concentra el **64,64 % de los ingresos totales**.

Mall of Istanbul registra la mayor facturación acumulada entre los centros comerciales analizados.

### Limitaciones

- Los datos de 2023 comprenden únicamente una parte del año, por lo que no permiten comparar ejercicios anuales completos.
- El dataset no incluye identificadores de productos individuales, lo que limita el análisis a nivel de categoría.
- Cada cliente aparece asociado a una única transacción, por lo que no es posible analizar la recurrencia de compra.

## Estructura del proyecto

```text
analisis-ventas-centros-comerciales/
├── centros_comerciales.ipynb
├── README.md
└── requirements.txt
```

Para ejecutar el análisis, el archivo CSV debe guardarse en una carpeta `data` dentro del directorio principal, con el nombre `datos_ventas_centros_comerciales.csv`.

## Cómo ejecutar el análisis

1. Descargar o clonar el repositorio.
2. Instalar las dependencias:

   `pip install -r requirements.txt`

3. Colocar el CSV en `data/datos_ventas_centros_comerciales.csv`.
4. Abrir `centros_comerciales.ipynb` en Jupyter Notebook o VS Code.
5. Ejecutar las celdas en orden, desde el inicio.

## Herramientas utilizadas

- **Python:** procesamiento y análisis de datos.
- **Pandas:** agrupaciones, cálculos, tratamiento de fechas y obtención de indicadores.
- **Jupyter Notebook:** desarrollo y documentación del análisis.
