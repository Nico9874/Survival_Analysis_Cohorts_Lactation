# Análisis de Duración de la Lactancia Materna y Factores Asociados

## Descripción  
Este proyecto analiza la **duración de la lactancia materna** y los factores que influyen en ella mediante **análisis exploratorio, curvas de supervivencia (Kaplan-Meier) y modelos de riesgos proporcionales de Cox**. El objetivo es identificar **patrones y factores clave** que afectan la lactancia, con aplicaciones en **políticas de salud**.

## Tecnologías utilizadas
- **Lenguaje / Framework**: R
- **Librerías o paquetes clave**:
  - `tidyverse`, `dplyr`, `ggplot2`, `tidyr`, `readr`: Manipulación y visualización de datos.
  - `survival`, `survminer`, `cohorts`: Modelado de supervivencia y visualización.
  - `viridis`, `lubridate`, `hms`: Transformaciones de datos y formatos de tiempo.
  - `quantreg`: Análisis de regresión cuantílica.
  - `forestmodel`: Creación de **Forest Plots** para interpretar el modelo de Cox.  

## Resultados clave  

### **1. Análisis Exploratorio**  
- **Duración promedio de la lactancia:**  
  - A las **12 semanas**: 42.0% de las madres siguen lactando.  
  - A las **24 semanas**: 21.6% de las madres continúan con lactancia.  
  - A las **36 semanas**: 13.1% de las madres mantienen la lactancia.  
- **Distribución por raza:** Se encontraron diferencias en la duración de la lactancia según grupo racial.  

### **2. Análisis de Supervivencia (Kaplan-Meier)**  
- **Curva de supervivencia global:**  
  - Muestra un **descenso progresivo** en la probabilidad de continuar con lactancia, con una caída más pronunciada en las primeras semanas.  
- **Comparación de curvas por raza:**  
  - **P-valor = 0.019** → Existen **diferencias significativas** entre grupos raciales.  
  - **Las madres blancas** presentan una mayor duración de lactancia.  
  - **Las madres negras** interrumpen la lactancia más rápidamente.  

### **3. Modelo de Riesgos Proporcionales de Cox**  
Se ajustó un **modelo de Cox** para evaluar el impacto de diferentes factores en la duración de la lactancia.

| Variable   | Hazard Ratio (HR) | p-valor | Interpretación  |
|------------|------------------|--------|----------------|
| **Raza**   | 1.15             | 0.002  | Las madres de ciertos grupos raciales tienen un 15% más de probabilidad de interrumpir la lactancia antes. |
| **Pobreza** | 0.83             | 0.040  | Las madres en pobreza tienen un 17% menos de probabilidad de interrumpir la lactancia. |
| **Fumar**   | 1.23             | 0.009  | Las madres fumadoras tienen un 23% más de riesgo de interrumpir la lactancia. |
| **Alcohol** | 1.20             | 0.131  | No es estadísticamente significativo. |
| **Educación** | 0.94           | 0.006  | Cada año adicional de educación reduce el riesgo de interrupción en un 6%. |
| **Edad**    | 1.02             | 0.159  | No muestra un impacto claro en la duración de la lactancia. |
| **Atención prenatal** | 0.98    | 0.860  | No tiene un efecto significativo. |

## Conclusión  
 **La duración de la lactancia está influenciada por factores como educación, tabaquismo, pobreza y raza**, mientras que **la edad y la atención prenatal no muestran un impacto claro**.  
 **Para prolongar la lactancia materna, se recomienda:**  
- **Programas educativos** sobre lactancia materna dirigidos a madres con menor acceso a educación.  
- **Estrategias para reducir el consumo de tabaco** en madres lactantes, incluyendo campañas de concienciación y apoyo médico.  
- **Apoyo social y económico** para madres en pobreza, garantizando que la lactancia sea una elección informada y no solo por necesidad.  
- **Fortalecer redes de apoyo** para la lactancia, con asesoramiento en hospitales y centros de salud.  

Estos hallazgos pueden **servir como base para diseñar políticas públicas** enfocadas en mejorar la **salud materno-infantil** y fomentar la **lactancia materna de manera más efectiva**. 🚀
