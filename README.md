# TFG DistilBERT - Clasificación temática de quasi-sentences

Este repositorio contiene el código final utilizado para entrenar, evaluar y aplicar un modelo DistilBERT a la detección del tópico tercera edad / pensiones en quasi-sentences de programas electorales.

## Objetivo

El objetivo del código es:

1. cargar los conjuntos train, validation y test;
2. entrenar modelos DistilBERT para clasificación binaria;
3. seleccionar hiperparámetros y umbral usando validación;
4. evaluar el modelo final en test;
5. aplicar el modelo al corpus para construir un indicador de saliencia.

## Archivos principales

- `notebook_original.ipynb`: notebook original de trabajo en Google Colab.
- `script_revisable.py`: versión lineal y revisable del pipeline.
- `data_sample/`: muestras reducidas de los datos reales.
- `outputs/phase2_results.json`: resultados principales de la fase 2.
- `notes/checklist_revision.md`: puntos concretos que debe revisar Codex.

## Entorno previsto

El código fue desarrollado para Google Colab, usando Hugging Face Transformers y Trainer.

## Advertencia

Los datos incluidos son muestras. El corpus completo no se incluye por tamaño y por restricciones de uso.
