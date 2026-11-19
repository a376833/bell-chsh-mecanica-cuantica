# Desigualdades de Bell y CHSH — Mecánica Cuántica

**Autora:** Aylin Fernanda Terán Díaz · Universidad Autónoma de Chihuahua

## Contenido

- `notebooks/01_simulacion_bell.ipynb`: notebook único, ejecutado y con resultados visibles.
- `figuras/`: cuatro figuras PNG producidas por el notebook, con los nombres usados en Overleaf.
- `datos/`: tablas CSV de los resultados, convergencia, ruido y eficiencia.
- `informe/ajustes_numericos_reporte.md`: cifras exactas para sincronizar el reporte LaTeX.

## Cómo reproducir

Requiere Python 3.10+ y Jupyter. Desde la raíz del repositorio:

```bash
python -m pip install -r requirements.txt
cd notebooks
jupyter notebook 01_simulacion_bell.ipynb
```

Seleccionar **Kernel → Restart & Run All**. Las figuras y CSV se guardan automáticamente en las carpetas correspondientes. Se usan NumPy, Matplotlib y Pandas; semilla base `42` y subsemillas deterministas por sección, por lo que los resultados no dependen del orden en que se ejecuten otras secciones.

## Reproducir cada figura

1. `figuras/correlacion_angular.png`: sección 1, 37 ángulos y 1000 pares por ángulo.
2. `figuras/convergencia_CHSH.png`: sección 2, N=100, 1000, 10000 y 100000 pares por combinación.
3. `figuras/comparacion_local_cuantica.png`: sección 3, comparación Monte Carlo y teoría local/cuántica.
4. `figuras/ruido_visibilidad_CHSH.png`: sección 4, nueve visibilidades, 100000 pares por combinación.

La sección 5 estudia pérdidas de detección independientes y aclara que seleccionar solo coincidencias no constituye una prueba libre de la laguna de detección. La sección 6 exporta los CSV.

## Convenciones y límites

Se usa `S=E(a,b)-E(a,b')+E(a',b)+E(a',b')`, con a=0°, a'=90°, b=45° y b'=135°. Para el singlete, `E_Q(θ)=-cos θ`, mientras que el modelo local explícito predice `E_L(θ)=-1+2θ/π` para 0≤θ≤π. Las estimaciones de muestra pueden sobrepasar ligeramente las cotas teóricas por fluctuaciones finitas. El muestreo cuántico parte de probabilidades teóricas y **no es un experimento físico ni una refutación independiente del realismo local**.

**Importante:** antes de entregar el PDF final, sincronizar las tablas y resultados con `informe/ajustes_numericos_reporte.md`.

## Historial de cambios

El ZIP no contiene metadatos `.git` ni puede crear retroactivamente un historial de commits. Conservar los commits previos del repositorio y subir los cambios de manera auténtica, sin inventar fechas.
