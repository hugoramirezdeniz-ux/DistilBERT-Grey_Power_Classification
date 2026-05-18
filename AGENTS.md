# Instrucciones para Codex

Este repositorio contiene código académico para un TFG de Economía que usa DistilBERT para clasificación binaria de quasi-sentences.

## Estilo de revisión

Prioriza:
1. Errores que puedan invalidar los resultados.
2. Riesgos de data leakage.
3. Inconsistencias entre entrenamiento, validación, test y aplicación al corpus.
4. Errores en métricas: accuracy, precision, recall, F1, FPR, TPR.
5. Errores de umbral y prevalencia estimada.
6. Problemas de reproducibilidad en Colab.

No hagas refactorizaciones cosméticas salvo que mejoren la claridad metodológica.

## Restricciones

- Mantener compatibilidad con Google Colab.
- No eliminar dependencias necesarias para Hugging Face Trainer.
- No cambiar la lógica metodológica sin justificarlo.
- No cargar datos externos.
- No modificar nombres de columnas sin avisar.
