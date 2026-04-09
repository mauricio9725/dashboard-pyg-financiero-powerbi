# 📊 Dashboard P&L Financiero — Power BI

Dashboard financiero de análisis de resultados construido completamente en Power BI a partir de datos en Excel. El modelo de datos, las métricas DAX y la arquitectura del reporte fueron diseñados desde cero.

---

## 🖼️ Vista previa

![Estado de Resultados](images/Estado%20de%20Resultados.png)
![Margen YTD por Linea y Producto](images/Margen%20YTD%20por%20linea%20y%20producto.png)
![Margen por Cliente](images/Margen%20por%20cliente.png)
![Análisis por Área Solicitante](images/Analisis%20por%20area%20solicitante.png)

---

## 🗂️ Contenido del reporte

| Página | Descripción |
|--------|-------------|
| 0. Guía Rápida | Definición de métricas, convenciones contables y notas de lectura |
| 1. Estado de Resultados | P&L mensual con desglose de ingresos, egresos y margen YTD |
| 2.1 Análisis Línea, Producto y Tipo Cuenta | Rentabilidad cruzada por línea de negocio y producto |
| 2.2 Margen YTD | Comparativo de margen acumulado por línea y producto |
| 3. Margen por Cliente | Ranking de clientes por margen con variación MoM |
| 4.1 Ingresos Línea y Top Inferior Clientes | Clientes con menor margen YTD por período seleccionado |
| 4.2 Análisis por Área Solicitante | Distribución de egresos por área mediante treemap |
| 5. Análisis | Conclusiones narrativas con hallazgos accionables del período |

---

## 🛠️ Tecnologías aplicadas

- **Power BI Desktop** — diseño y desarrollo completo del reporte
- **Power Query (M)** — transformación y normalización de datos desde Excel
- **DAX** — métricas de ingresos, egresos, margen, YTD y variación MoM
- **Modelado estrella** — construido desde cero con tablas de hechos y dimensiones
- **Data storytelling** — página de análisis narrativo con conclusiones accionables

---

## 📐 Modelo de datos

Modelo estrella diseñado desde cero a partir de un archivo Excel plano:

| Tabla | Tipo | Descripción |
|-------|------|-------------|
| `Fact_Financiera` | Hecho | Transacciones financieras (débito/crédito) |
| `Dim_Calendario` | Dimensión | Tiempo con soporte para YTD y MoM |
| `Dim_Cliente` | Dimensión | Clientes de la organización |
| `Dim_Linea` | Dimensión | Líneas de negocio |
| `Dim_Producto` | Dimensión | Productos por línea |
| `Dim_Cuenta_Contable` | Dimensión | Cuentas del P&L |
| `Dim_Tipo_Cuenta` | Dimensión | Clasificación Ingreso / Egreso |
| `Estructura_PyG` | Dimensión | Jerarquía del estado de resultados |
| `Tabla_DAX` | Soporte | Tabla de medidas centralizadas |

---

## 📏 Métricas principales (DAX)

- **Ingresos / Egresos (Mes):** suma del período seleccionado
- **Margen (Mes):** Ingresos − Egresos
- **Margen % (Mes):** Margen / Ingresos
- **YTD:** acumulado desde el 01/01 del año hasta el período seleccionado
- **Variación MoM:** cambio mes a mes en margen absoluto

---

## 💡 Hallazgos clave

- **Servicios Ciudadanos Digitales** es la línea más rentable con un margen YTD ampliamente superior al resto
- **LCRC y LICCCEAS** son los productos con mayor contribución al margen
- Tres líneas operan con margen negativo en el acumulado YTD, requiriendo revisión de mix, pricing o clasificación de cuentas
- El análisis por área solicitante permite identificar los centros de costo con mayor impacto en egresos

---

## 👤 Autor

**Hernán Mauricio Bustos**  
BI Senior | SQL Avanzado | Data Analytics  
[LinkedIn](https://www.linkedin.com/in/mauricio-bustos) | [Portfolio](https://mauricio9725.github.io)
