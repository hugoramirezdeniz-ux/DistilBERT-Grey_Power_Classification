# Checklist de revisión

## 1. Datos

- [ ] Comprobar que las etiquetas se llaman `labels`.
- [ ] Comprobar que `labels` toma valores enteros 0/1.
- [ ] Comprobar que no hay mezcla de manifiestos entre train, validation y test.
- [ ] Comprobar que `manifesto_id` no entra como feature del modelo.
- [ ] Comprobar que `text_en` es la columna usada para tokenizar.

## 2. Tokenización

- [ ] Revisar max_length.
- [ ] Revisar truncation y padding.
- [ ] Comprobar que la tokenización no elimina columnas necesarias antes de tiempo.

## 3. Entrenamiento

- [ ] Revisar TrainingArguments.
- [ ] Comprobar compatibilidad con Colab.
- [ ] Comprobar que se guarda el mejor checkpoint si se espera usarlo.
- [ ] Comprobar comportamiento si no hay mejor checkpoint guardado.
- [ ] Revisar seed.

## 4. Métricas

- [ ] Comprobar que precision, recall y F1 se calculan para la clase positiva.
- [ ] Comprobar que FPR se calcula como FP / (FP + TN).
- [ ] Comprobar que el barrido de umbrales usa validación, no test.
- [ ] Comprobar que el test solo se usa al final.

## 5. Inferencia

- [ ] Comprobar que se aplica softmax correctamente.
- [ ] Comprobar que se guarda la probabilidad de clase positiva.
- [ ] Comprobar que se guarda la etiqueta predicha según el umbral elegido.
- [ ] Comprobar que las predicciones pueden unirse de nuevo al corpus mediante `id`, `manifesto_id` y `qs_order`.

## 6. Reproducibilidad

- [ ] Comprobar requirements.
- [ ] Comprobar rutas relativas.
- [ ] Comprobar que el script puede ejecutarse sin depender de estado oculto del notebook.
