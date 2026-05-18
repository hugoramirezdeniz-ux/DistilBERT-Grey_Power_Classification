# Contexto metodológico

El proyecto entrena un clasificador binario para identificar quasi-sentences relacionadas con tercera edad / pensiones.

## Unidad de análisis

La unidad de análisis es la quasi-sentence.

## Etiqueta

- 1: quasi-sentence relacionada con tercera edad / pensiones.
- 0: quasi-sentence no relacionada.

## Modelo

Se usa `distilbert-base-uncased` mediante Hugging Face Transformers.

## Partición de datos

Los cojuntos train/validation/test han sido extraido tras una partición por manifiesto previa, evitando el leakage.

## Selección de modelo

La selección de hiperparámetros se realiza en validación. El test se reserva para la evaluación final.

## Umbral

El umbral de clasificación puede diferir de 0.5 y debe seleccionarse usando el conjunto de validación.

## Métricas relevantes

Además de precisión, se priorizan métricas de la clase positiva:

- accuracy;
- recall;
- F1;
- FPR;
- prevalencia real;
- prevalencia predicha.

El FPR es especialmente importante porque la saliencia real del tópico suele ser baja.
