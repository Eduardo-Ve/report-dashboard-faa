# Incidentes aéreos con fauna silvestre (FAA) – Minería de Datos

Proyecto de minería de datos (Duoc UC, MINERIA DE DATOS 001D, profesor Carlos Correa) sobre la
[FAA Wildlife Strike Database](https://wildlife.faa.gov/search) (1990–2023, +280.000 registros).

**Autores:** Eduardo Velásquez, Willy Castro

## Objetivo
Entender los choques entre aeronaves y fauna silvestre y predecir si un impacto causa daño a la aeronave (`INDICATED_DAMAGE`).

## Metodología (CRISP-DM)
1. Comprensión del negocio
2. Comprensión de los datos: nulos, outliers, correlaciones
3. Preparación: imputación (moda/media), winsorización, label encoding, SMOTE
4. Modelamiento
   - Clasificación: SVM, Random Forest, Gradient Boosting
   - Regresión (`DISTANCE`): regresión lineal múltiple, árbol de decisión
   - No supervisado: K-Means (codo, silueta, Davies-Bouldin) + PCA

## Estructura
```
notebooks/wildlife_strikes_faa.ipynb   # análisis completo
data/                                  # colocar aquí el CSV (no versionado)
requirements.txt
```

## Cómo ejecutar
1. Descargar el dataset desde la FAA y guardarlo en `data/`.
2. `pip install -r requirements.txt`
3. Abrir el notebook. Fue escrito en Google Colab: la celda de carga usa `google.colab.files.upload()`;
   fuera de Colab reemplazarla por `pd.read_csv("data/<archivo>.csv")`.

## Notas
- Los datos no se incluyen en el repositorio por tamaño y licencia.
