# Instrucciones para Codex

## Contexto del proyecto

Este repositorio forma parte de un TFG de Economía aplicado a PLN y ciencia política. El objetivo es revisar el código final de un clasificador DistilBERT para detectar quasi-sentences relacionadas con tercera edad / pensiones en programas electorales.

## Objetivo de la revisión

Revisar `script_revisable.py` para detectar:

1. errores técnicos;
2. incoherencias metodológicas;
3. problemas de reproducibilidad;
4. errores en métricas;
5. riesgos de data leakage;
6. problemas en la selección de hiperparámetros y umbral;
7. problemas al guardar/cargar el mejor modelo;
8. errores al aplicar el modelo al corpus.

## Restricciones importantes

- Mantener compatibilidad con Google Colab.
- No transformar el proyecto en un paquete complejo si no es necesario.
- No cambiar la metodología sustantiva salvo que haya un error claro.
- No modificar nombres de columnas sin justificarlo.
- Mantener la variable objetivo como `labels`, con valores enteros 0/1.
- Mantener `manifesto_id` fuera de los inputs del modelo, pero usarlo para controlar particiones.
- No usar el conjunto test para elegir hiperparámetros ni umbral.
- No ejecutar entrenamientos largos.
- Usar los archivos de `data_sample/` solo para pruebas estructurales.

## Criterios metodológicos clave

- El umbral debe seleccionarse en validación.
- El test debe reservarse para evaluación final.
- Deben reportarse métricas de clase positiva: precision, recall, F1 y FPR.
- Debe comprobarse que las predicciones agregadas permiten construir saliencia por manifiesto.

## Estilo de cambios

Antes de modificar el código, identificar claramente el problema.
Después de modificarlo, explicar:
- qué se cambió;
- por qué;
- qué riesgo corrige;
- si afecta o no a la metodología del TFG.
