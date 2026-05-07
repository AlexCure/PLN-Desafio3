# TP3 - Procesamiento de Lenguaje Natural

## Alumno

Alex Martín CURELLICH - SIU a2214

## Descripción

Trabajo práctico sobre modelado de lenguaje utilizando **redes neuronales recurrentes** para generación automática de texto a nivel carácter.

Se entrenaron y compararon distintos modelos recurrentes (**SimpleRNN, LSTM y GRU**) utilizando como corpus la obra *Viaje al centro de la Tierra* de Julio Verne.  
Además, se implementaron distintas estrategias de generación de secuencias para analizar su comportamiento y calidad de generación.

---

## Contenido

El trabajo incluye los siguientes puntos:

1. **Preprocesamiento del corpus**

   * Obtención del texto desde una fuente web
   * Limpieza y normalización
   * Tokenización a nivel carácter
   * División en conjuntos de entrenamiento y validación

2. **Entrenamiento de modelos recurrentes**

   * SimpleRNN
   * LSTM
   * GRU
   * Comparación de desempeño utilizando perplexity

3. **Generación de secuencias**

   * Greedy Search
   * Beam Search determinístico
   * Beam Search estocástico

4. **Análisis del efecto de la temperatura**

   * Temperaturas bajas
   * Temperaturas medias
   * Temperaturas altas
   * Impacto sobre coherencia y diversidad del texto generado

---

## Desarrollo

Para el entrenamiento se utilizó como corpus la novela *Viaje al centro de la Tierra* de Julio Verne.

Se evaluaron tres arquitecturas recurrentes distintas manteniendo constantes los principales hiperparámetros de entrenamiento, permitiendo comparar el impacto de cada arquitectura sobre la calidad del modelo.

Finalmente, se seleccionó el modelo GRU para la generación de texto debido a su mejor desempeño en términos de perplexity y calidad de secuencias generadas.

---

## Requisitos

El notebook fue adaptado para poder ejecutarse de forma sencilla en Google Colab. Sin embargo, para su desarrollo en entorno local se utilizó un entorno virtual.

En caso de optar por la ejecución local, se deben seguir las siguientes indicaciones.

El proyecto utiliza **Poetry** para la gestión de dependencias.

**Instalación:**

```bash
poetry install
```

**Ejecución:**

```bash
poetry run jupyter notebook
```