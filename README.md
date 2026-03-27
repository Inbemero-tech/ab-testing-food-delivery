# 📱 Análisis de Comportamiento y A/B Testing
**Stack:** Python (Pandas, Scipy, Plotly)

Este proyecto analiza el impacto de un cambio de diseño en una aplicación de alimentos.
Se procesaron más de 240k registros para evaluar el embudo de ventas y la retención.

## 🎯 Objetivo del Negocio
* **Analizar el embudo de conversión** para detectar fugas críticas de usuarios en el proceso de compra.
* **Evaluar los resultados de un test A/A/B** utilizando métodos de estadística inferencial para validar cambios en la interfaz.
* **Alineación con Riesgo:** Asegurar que las modificaciones en el producto no introduzcan riesgos operativos, sesgos de comportamiento o caídas en la rentabilidad del negocio.

## 🛠️ Stack Tecnológico
* **Lenguaje:** Python 🐍
* **Librerías de Análisis:** `Pandas`, `Numpy`
* **Estadística:** `Scipy.stats` (Z-test)
* **Visualización:** `Matplotlib`, `Seaborn`, `Plotly`

## 📈 Hallazgos Clave (Data Insights)
* **Embudo Crítico:** Se identificó que el **38% de los usuarios se pierden después de la pantalla de inicio**. Esta es la zona de mayor riesgo identificada para la retención del negocio.
* **Consistencia de Datos:** Se implementó una limpieza profunda y filtrado de periodos incompletos para evitar sesgos temporales, trabajando con un dataset robusto de **~240,000 eventos**.

## ⚖️ Metodología de Experimentación
> *Este apartado destaca el rigor analítico aplicado para garantizar la fiabilidad de los resultados.*

1. **Validación A/A:** Comparación de dos grupos de control para asegurar que la división de usuarios fuera equitativa y el mecanismo de test fuera fiable antes de evaluar el cambio.
2. **Test A/B:** Utilización de la **Prueba Z para Proporciones** para comparar los grupos de control contra el grupo de prueba.
3. **Control de Riesgo Estadístico:** Implementación de la **Corrección de Bonferroni** para ajustar el nivel de significancia ($\alpha = 0.05$) ante la ejecución de múltiples comparaciones, mitigando el riesgo de **Error Tipo I (falsos positivos)**.

## ✅ Conclusión del Proyecto
> "No se encontró evidencia estadística suficiente para rechazar la hipótesis nula. El cambio de fuente es seguro para el despliegue, ya que no altera significativamente el comportamiento del usuario ni la tasa de conversión final ($p > \text{umbral corregido}$)."
