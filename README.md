# Tarea3-BigData-Grupo30# Tarea 3 - Procesamiento de Datos con Apache Spark

**Curso:** Big Data  
**Grupo:** 30  
**Integrantes:** [nombres de quienes participaron]

## Descripción
Procesamiento batch y streaming con Apache Spark sobre el conjunto de datos
Bank Marketing (UCI), adaptado a Google Colab por dificultades técnicas con la
máquina virtual del curso.

## Dataset
Moro, S., Rita, P., & Cortez, P. (2014). Bank Marketing [Conjunto de datos].
UCI Machine Learning Repository. https://doi.org/10.24432/C5K306

- 41.188 registros, 21 variables, separador `;`

## Componente batch
- Limpieza: eliminación de duplicados y tratamiento de valores `unknown`
- Transformación: variable objetivo, grupos de edad, duración en minutos
- Análisis: tasas de conversión por ocupación, edad, estado civil, mes y campaña previa
- Visualización: cuatro gráficos de barras

## Componente streaming
- Kafka 3.7.1 en modo KRaft, topic `sensor_data`
- Spark Structured Streaming con ventanas de 1 minuto
- 75 eventos procesados, promedios de temperatura y humedad por sensor

## Cómo ejecutar
1. Abrir el cuaderno en Google Colab
2. Ejecutar las celdas en orden
3. Subir `archive.zip` cuando se solicite

## Resultados principales
- Tasa de conversión global: 11,27 %
- Estudiantes: 31,43 % | Jubilados: 25,26 %
- Campaña previa exitosa: 65,11 %

## Diferencia con el anexo
Se usó KRaft en lugar de ZooKeeper y se convirtió el campo `timestamp`
a tipo fecha antes de aplicar `window()`, requisito de Spark.
