# Revisión notebook TFG DistilBERT

Este proyecto contiene un notebook de Colab para entrenar, seleccionar y aplicar un modelo DistilBERT a una tarea de clasificación binaria de quasi-sentences.

## Objetivo metodológico

Clasificar quasi-sentences según si tratan sobre tercera edad, pensiones o retiro. El modelo final se selecciona en fase 2 usando métricas de validación y después se aplica al corpus completo para construir un indicador de saliencia.

## Flujo esperado

1. Cargar datasets de entrenamiento, validación y test.
2. Entrenar varios modelos en fase 1.
3. Seleccionar los mejores modelos.
4. Ejecutar fase 2.
5. Guardar `phase2_results.json`.
6. Cargar el modelo ganador desde `final_model`.
7. Aplicar el modelo al corpus completo.
8. Guardar predicciones con probabilidad, etiqueta predicha, manifesto_id y qs_order.

## Aspectos críticos a revisar

- Consistencia entre `phase2_results.json`, `final_model` y el umbral final.
- Ausencia de data leakage entre train, validation y test.
- Correcta conservación de `manifesto_id` y `qs_order`.
- Correcta aplicación por batches al corpus.
