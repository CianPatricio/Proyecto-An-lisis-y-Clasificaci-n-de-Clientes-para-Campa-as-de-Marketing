# 🎯 Análisis y Clasificación de Clientes para Campañas de Marketing

Proyecto de ciencia de datos que **segmenta clientes** según su edad, ingresos y nivel de gasto usando aprendizaje no supervisado (PCA, SVD, K-Means y clustering jerárquico), para diseñar **estrategias de marketing diferenciadas** por grupo.

![Python](https://img.shields.io/badge/Python-3.x-blue)
![scikit-learn](https://img.shields.io/badge/scikit--learn-ML-orange)
![Jupyter](https://img.shields.io/badge/Jupyter-Notebook-F37626)

---

## 📌 Objetivo

Identificar grupos de clientes con comportamientos similares para personalizar campañas, ofertas y canales de comunicación en lugar de aplicar una misma estrategia a todos.

## 📂 Dataset

Archivo `customer_data.csv` con **200 clientes** y sin valores faltantes.

| Columna | Descripción |
|---|---|
| `ID Cliente` | Identificador del cliente (1 a 200) |
| `Edad` | Edad del cliente (18 a 69 años, promedio cercano a 43) |
| `Ingresos Anuales (k$)` | Ingresos anuales en miles de dólares (20 a 119, promedio cercano a 70) |
| `Puntuación de Gasto (1-100)` | Puntaje de gasto del cliente (1 a 99, promedio cercano a 50) |
| `Categoría de Producto Favorito` | Categoría preferida (por ejemplo Libros, Hogar, Electrónica) |

## 🔄 Metodología

1. **Preparación**: revisión de la estructura y estadísticas descriptivas, y normalización de `Edad`, `Ingresos` y `Puntuación de Gasto` con `MinMaxScaler`.
2. **Reducción de dimensiones**: PCA con 2 componentes y SVD (`numpy.linalg.svd`) para representar los datos en 2D.
3. **Clustering**: K-Means con 3 clusters (`random_state=42`) y clustering jerárquico con enlace de Ward.
4. **Visualización**: gráfico de dispersión de los componentes principales coloreado por cluster y dendrograma del clustering jerárquico.
5. **Interpretación**: perfil promedio de cada cluster y estrategias de marketing sugeridas.

## 📊 Resultados: segmentos encontrados

| Cluster | Edad media | Ingresos medios (k$) | Gasto medio | Perfil |
|---|---|---|---|---|
| **0** | 43 | 52.51 | 20.17 | Ingresos medios y **gasto bajo** |
| **1** | 34 | 49.08 | 72.20 | Clientes más jóvenes, ingresos medios y **gasto alto** |
| **2** | 50 | 97.33 | 62.00 | Clientes de mayor edad, **ingresos altos** y gasto medio-alto |

## 💡 Estrategias de marketing sugeridas

- **Cluster 1 (jóvenes, gasto alto)**: marketing digital intensivo (redes sociales, influencers), productos innovadores y eventos o experiencias exclusivas.
- **Cluster 2 (mayor edad, ingresos altos)**: productos premium, comunicación personalizada y directa, y programas de fidelidad con beneficios exclusivos.
- **Cluster 0 (gasto bajo)**: ofertas y descuentos que activen el consumo, comunicación centrada en valor y accesibilidad.

## 🚀 Cómo ejecutarlo

```bash
# 1. Clonar el repositorio
git clone https://github.com/<tu-usuario>/<nombre-del-repo>.git
cd <nombre-del-repo>

# 2. Instalar dependencias
pip install pandas numpy matplotlib seaborn scikit-learn scipy jupyter

# 3. Abrir el notebook
jupyter notebook "Proyecto_Análisis_y_Clasificación_de_Clientes_para_Campañas_de_Marketing.ipynb"
```

> Asegurate de que `customer_data.csv` esté en la misma carpeta que el notebook.

## 🛠️ Tecnologías

Python · pandas · NumPy · matplotlib · seaborn · scikit-learn · SciPy · Jupyter Notebook

## 🔭 Próximos pasos

- Justificar el número de clusters con el **método del codo** y el **coeficiente de silueta**, en lugar de fijarlo en 3.
- Incorporar la variable `Categoría de Producto Favorito` (por ejemplo con codificación one-hot) al análisis.
- Comparar la partición de K-Means con la del clustering jerárquico.
- Medir el impacto real de cada estrategia con pruebas A/B.

## 👤 Autor

**Patricio Ruben Cian** · Analista Universitario en Sistemas de Computación · [LinkedIn](https://www.linkedin.com/in/<tu-perfil>) · [GitHub](https://github.com/<tu-usuario>)
