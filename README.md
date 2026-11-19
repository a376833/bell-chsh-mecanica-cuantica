# Desigualdades de Bell y experimentos sin lagunas

**Aylin Fernanda Terán Díaz**  
Licenciatura en Ingeniería Física · Universidad Autónoma de Chihuahua

## Descripción

En este proyecto estudio las correlaciones del estado singlete y la desigualdad CHSH mediante simulaciones Monte Carlo. Comparo la predicción cuántica con un modelo de variables ocultas locales y analizo cómo influyen el número de mediciones, el ruido y la eficiencia de detección.

Para las orientaciones elegidas, el límite de los modelos locales es $|S|\leq 2$, mientras que la predicción cuántica alcanza $2\sqrt{2}$.

## Archivos

- `notebooks/01_simulacion_bell.ipynb`: simulaciones y cálculos.
- `figuras/`: gráficas generadas con Python.
- `datos/`: resultados numéricos exportados en CSV.
- `informe/resultados_numericos.md`: resumen de los valores obtenidos.
- `requirements.txt`: bibliotecas necesarias.

## Ejecución

Se necesita Python y Jupyter Notebook. Desde la carpeta principal del repositorio:

```bash
python -m pip install -r requirements.txt
cd notebooks
jupyter notebook 01_simulacion_bell.ipynb
```

En Jupyter se puede ejecutar el notebook completo con **Restart & Run All**. Las gráficas se guardan en `figuras/` y las tablas en `datos/`.

La simulación utiliza una semilla base de 42 y generadores independientes para las distintas secciones. De esta forma, los resultados son reproducibles con el mismo código y las mismas versiones de las bibliotecas.

## Simulaciones realizadas

1. **Correlación angular:** comparación entre $E_Q(\theta)=-\cos\theta$ y los resultados de Monte Carlo.
2. **Parámetro CHSH:** estimación de $S$ y estudio de las fluctuaciones al cambiar el número de pares simulados.
3. **Modelo local:** comparación con $E_L(\theta)=-1+2\theta/\pi$ para $0\leq\theta\leq\pi$.
4. **Visibilidad:** variación de $|S|$ al introducir ruido en las correlaciones.
5. **Eficiencia de detección:** estudio de las coincidencias registradas al introducir pérdidas independientes.

## Alcance

Las simulaciones cuánticas utilizan las probabilidades teóricas del estado singlete. Por ello, sirven para estudiar las predicciones de la mecánica cuántica, pero no sustituyen una prueba experimental de Bell. Asimismo, el análisis de pérdidas independientes no demuestra por sí mismo el cierre de la laguna de detección.

### Reproducción de una figura experimental

Se reprodujo la Figura 4a del artículo de Hensen et al. (2015), *Loophole-free Bell inequality violation using electron spins separated by 1.3 kilometres*, utilizando los conteos experimentales publicados.

A partir de estos datos se calcularon las cuatro correlaciones correspondientes a las configuraciones de medición CHSH, obteniendo \(S=2.4225\), consistente con el resultado reportado de \(S=2.42\pm0.20\).

La reproducción se realizó mediante Python e incluye las correlaciones experimentales y sus incertidumbres estadísticas. El procedimiento permite verificar numéricamente la violación de la desigualdad CHSH a partir de los datos originales.
