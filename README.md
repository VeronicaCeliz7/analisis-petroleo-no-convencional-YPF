https://veronicaceliz7.github.io/analisis-petroleo-no-convencional-YPF/
# Análisis Descriptivo de Producción No Convencional

Análisis exploratorio de datos de producción mensual de pozos no 
convencionales de petróleo, gas y agua en Argentina (Vaca Muerta), 
utilizando el dataset público de la Secretaría de Energía.

## Sobre el proyecto

Este repositorio contiene el análisis descriptivo de tres variables 
de producción: petróleo (`prod_pet`), gas (`prod_gas`) y agua (`prod_agua`). 
Para cada una se calcularon medidas de tendencia central, dispersión, 
forma (skew y curtosis), y se generaron gráficos (histogramas y boxplots) 
con interpretación contextual.

El dataset es **solo de producción no convencional** (Vaca Muerta), 
cubriendo aproximadamente 20 años y 426.090 registros mensuales.

## Estructura del repositorio


```
.
├── notebooks/
│   ├── petroleo.ipynb    # Análisis de producción de petróleo
│   ├── gas.ipynb         # Análisis de producción de gas
│   └── agua.ipynb        # Análisis de producción de agua
└── README.md
```



## Cómo reproducir el análisis

### 1. Obtener el dataset

El dataset no se incluye en este repositorio por su tamaño (140 MB). 
Se puede descargar desde el portal de datos abiertos de la 
Secretaría de Energía:

[Descargar dataset: Producción de petróleo y gas por pozo](http://datos.energia.gob.ar/dataset/produccion-de-petroleo-y-gas-por-pozo/archivo/b5b58cdc-9e07-41f9-b392-fb9ec68b0725)

**Fuente:** Secretaría de Energía de la Nación  
**Dataset:** Producción de petróleo y gas por pozo  
**Registros:** 426.090  
**Período:** 2006 - 2025 (aproximadamente 20 años)

### 2. Abrir los notebooks

**Opción recomendada: Google Colab**

1. Entrar a [colab.research.google.com](https://colab.research.google.com/).
2. Subir el archivo `.ipynb` que quieras ejecutar.
3. Cargar el dataset desde Drive o desde el PC.
4. Ejecutar las celdas de arriba hacia abajo.

**Opción alternativa: local**

Requiere Python 3 con:

```bash
pip install pandas numpy matplotlib seaborn
```

## Requisitos

- Python 3.8 o superior
- pandas
- numpy
- matplotlib
- seaborn

## Principales hallazgos

- Las tres variables presentan **sesgo positivo extremo** (skew > 4), lo que indica que la mayoría de los pozos producen poco y unos pocos concentran la mayor parte del volumen.
- La **producción de agua** es la más asimétrica (skew = 7,87) y la de colas más gruesas (curtosis = 113,48).
- La **producción de gas** presenta una distribución fuertemente asimétrica (skew = 5,46) con colas gruesas (curtosis = 40,62).
- La **producción de petróleo** tiene un comportamiento similar (skew = 4,92, curtosis = 34,29).
- Los **valores atípicos** son frecuentes y corresponden a pozos altamente productivos, característicos de la producción no convencional (Vaca Muerta).

## Autor

**Veronica Celiz**  
Analista de Sistemas (tercer año)  
veronicacelizanalista@gmail.com
