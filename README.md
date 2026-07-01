# Telemarketing

# Análisis Inteligente de Datos – Trabajo Práctico N° 1

Trabajo práctico obligatorio de la materia **Análisis Inteligente de Datos** (Maestría en Exploración de Datos y Descubrimiento del Conocimiento). El objetivo es aplicar técnicas de muestreo, estadística descriptiva, visualización, pruebas de hipótesis y regresión lineal sobre un dataset real, utilizando R.

## Dataset

- **Nombre:** ML Marathon Dataset (Azure Developer Community)
- **Fuente:** Microsoft Azure
- **Año de publicación:** 2022
- **Tipo:** Base de datos abierta, formato CSV, matricial, multivariada

El dataset contiene información de una **institución financiera** que llevó adelante campañas de **marketing telefónico (telemarketing)** para ofrecer a sus clientes la contratación de un **depósito a plazo fijo**. Cada fila representa un cliente contactado durante una o más campañas, e incluye datos sociodemográficos, información sobre su situación bancaria y detalles del contacto realizado.

El objetivo del análisis es caracterizar a los clientes según si finalmente contrataron o no el depósito, y explorar qué variables se asocian con esa decisión.

**Principales variables del dataset:**

| Variable | Descripción |
|---|---|
| `age` | Edad del cliente |
| `job` | Tipo de ocupación/empleo |
| `marital` | Estado civil (casado, soltero, divorciado) |
| `education` | Nivel educativo (primary, secondary, tertiary, unknown) |
| `default` | Si el cliente tiene crédito en incumplimiento (default) |
| `balance` | Saldo promedio anual en la cuenta bancaria |
| `housing` | Si el cliente tiene préstamo hipotecario |
| `loan` | Si el cliente tiene préstamo personal |
| `contact` | Tipo de contacto utilizado (celular, teléfono fijo, etc.) |
| `duration` | Duración en segundos del último contacto telefónico |
| `campaign` | Cantidad de contactos realizados durante la campaña actual |
| `pdays` | Días transcurridos desde el último contacto de una campaña anterior |
| `previous` | Cantidad de contactos realizados antes de la campaña actual |
| `poutcome` | Resultado de la campaña de marketing anterior |
| `deposit` | **Variable objetivo**: indica si el cliente contrató (`yes`) o no (`no`) el depósito a plazo |

Sobre esta base, se generó una **muestra aleatoria estratificada y balanceada por `deposit`** (1000 casos por cada nivel, n = 2000 en total), utilizando una semilla fija para garantizar la reproducibilidad. Todo el trabajo práctico se desarrolla sobre esta muestra.

## Contenido del trabajo

A partir de una muestra aleatoria estratificada y balanceada por la variable `deposit` (n = 2000, semilla fija), se desarrollan los siguientes puntos:

1. Generación de la muestra estratificada y balanceada
2. Análisis estadístico descriptivo de variables numéricas por nivel de `deposit` (media, mediana, moda, varianza, asimetría, curtosis, etc.)
3. Representación gráfica de las variables numéricas
4. Tabla de frecuencias y porcentajes de `marital` según `deposit`
5. Gráfico de la tabla de frecuencias
6. Test de asociación entre dos variables continuas categorizadas
7. Test de asociación entre `education` y otra variable categórica
8. Intervalo de confianza (95%) para la diferencia de medias según `deposit`
9. Test de hipótesis para la diferencia de medias
10. Test de hipótesis sobre una muestra estratificada de 30 elementos
11. Comparación de la duración según nivel educativo (ANOVA / test no paramétrico + verificación de supuestos)
12. Regresión lineal simple entre dos variables cuantitativas
13. Informe final de conclusiones (500–800 palabras)

## Tecnologías y librerías utilizadas

- **R** (R Markdown)
- `dplyr` – manipulación de datos
- `readr` – lectura de archivos CSV
- `e1071` – asimetría y curtosis
- `modeest` – cálculo de la moda
- `corrplot` – visualización de correlaciones
- `kableExtra` – formato de tablas

