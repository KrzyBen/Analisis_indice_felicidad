Carpeta de logs de entrenamiento

Esta carpeta se utiliza para almacenar los logs generados durante el proceso de entrenamiento
del modelo de Deep Learning.

Los archivos contenidos en esta carpeta son generados automáticamente por TensorBoard y
corresponden a métricas como:
- pérdida (loss)
- precisión (accuracy)
- métricas de validación por época

Uso en el proyecto

Durante la ejecución del proyecto mediante Docker, TensorBoard se configura para leer los logs
desde la siguiente ruta interna del contenedor:

/app/logs/fit

Esta carpeta se encuentra inicialmente vacía y se llena automáticamente al entrenar el modelo.

Notas importantes

- Los archivos generados en esta carpeta no deben ser modificados manualmente.
- El contenido de esta carpeta puede variar entre ejecuciones.
- No es necesario versionar los archivos de logs; este README existe únicamente para preservar
  la estructura del proyecto en el repositorio.
