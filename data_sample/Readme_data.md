# Descripción de los datos de muestra

Los archivos incluidos son muestras reducidas de los conjuntos reales.

## Columnas esperadas

- `id`: identificador de quasi-sentence.
- `manifesto_id`: identificador del programa electoral.
- `qs_order`: posición de la quasi-sentence dentro del manifiesto.
- `text_en`: texto en inglés.
- `labels`: etiqueta binaria, 0 o 1.

## Notas

- Las muestras no preservan necesariamente la distribución completa del corpus.
- El objetivo de estos archivos es permitir pruebas estructurales del pipeline.
- No deben usarse para interpretar resultados sustantivos.
