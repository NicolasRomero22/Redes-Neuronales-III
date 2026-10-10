# Redes Neuronales III

**Optimización, regularización y evaluación de modelos de Deep Learning**

Especialización en Inteligencia Artificial · Percepción Computacional
Autor(es): Nombre Apellido

## Objetivo

Aplicar técnicas de optimización, regularización y evaluación sobre una red
neuronal en TensorFlow + Keras, usando el dataset MNIST. El trabajo compara
optimizadores e hiperparámetros, controla el overfitting con Dropout, L2 y
Early Stopping, y evalúa el modelo con Accuracy, Precision, Recall, F1 y
matriz de confusión.

## Dataset

**MNIST**: 70.000 imágenes de dígitos manuscritos de 28 × 28 píxeles
(clases 0 a 9). Se carga directamente con `keras.datasets.mnist`, por lo que
no hay que descargar nada manualmente.

| Conjunto | Imágenes | Uso |
|----------|----------|-----|
| Train    | 48.000   | Entrenar (actualiza pesos) |
| Dev      | 12.000   | Comparar configuraciones |
| Test     | 10.000   | Evaluación final |

La partición Train/Dev es estratificada (80/20) y las imágenes se
normalizan a [0, 1].

## Contenido del repositorio

| Archivo | Descripción |
|---------|-------------|
| `TallerRedesNeuronalesIII.ipynb` | Notebook con todas las prácticas ejecutadas |
| `Informe_Redes_Neuronales_III.pdf` | Informe técnico con resultados y análisis |
| `README.md` | Este archivo |

## Requisitos

- Google Colab (recomendado) o Python 3.10+
- tensorflow / keras
- scikit-learn
- pandas
- numpy
- matplotlib

Instalación local (opcional):

    pip install tensorflow scikit-learn pandas numpy matplotlib

## Orden de ejecución

1. Abrir el notebook en Google Colab:
   [Abrir en Colab](https://colab.research.google.com/github/NicolasRomero22/Redes-Neuronales-III/blob/main/TallerRedesNeuronalesIII.ipynb)
2. Ejecutar todas las celdas en orden (**Entorno de ejecución → Ejecutar todo**).
3. El notebook se organiza en estos laboratorios:
   - **A.** Datos, preprocesamiento y baseline
   - **B.** Optimización (SGD, RMSprop, Adam) y learning rate
   - **C.** Regularización (Dropout, L2, Early Stopping)
   - **D.** Métricas de evaluación y matriz de confusión
   - **E.** Diagnóstico de bias y variance

Semilla fija (`SEED = 42`); pueden aparecer pequeñas diferencias entre
entornos o hardware.

## Resultados principales

| Experimento | Resultado |
|-------------|-----------|
| Baseline (Dev accuracy) | 0,9657 |
| Mejor optimizador en Dev | RMSprop 0,9680 / Adam 0,9673 / SGD 0,9558 |
| Mejor learning rate (Adam) | 0,001 |
| Early Stopping | Detenido en la época 8 (pesos de la época 6) |
| Accuracy en Test (modelo final) | 0,9649 |
| F1 macro en Test | 0,9646 |

## Informe

📄 [Informe_Redes_Neuronales_III.pdf](Informe_Redes_Neuronales_III.pdf)
