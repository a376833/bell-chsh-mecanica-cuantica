# Cambios necesarios en el LaTeX (notebook ejecutado, semilla base 42)

**No entregar el reporte anterior con las cifras antiguas junto a este notebook.** Las siguientes cifras se obtuvieron ejecutando `notebooks/01_simulacion_bell.ipynb` completo.

## Tabla CHSH, N=10 000

| Correlación | Simulado |
|---|---:|
| E(a,b) | -0.7064 |
| E(a,b') | +0.6930 |
| E(a',b) | -0.7134 |
| E(a',b') | -0.7028 |

S = -2.8156, |S|=2.8156. Reemplazar **todas** las menciones a -2.8506 / 2.8506, incluida la comparación con experimentos.

## Tabla convergencia

| N | |S| | ΔS |
|---:|---:|---:|
| 100 | 2.8400 | 0.0116 |
| 1000 | 2.8420 | 0.0136 |
| 10000 | 2.8300 | 0.0016 |
| 100000 | 2.8303 | 0.0019 |

Modificar el párrafo explicativo: para N=1000 el error fue ligeramente **mayor** que para N=100; para N=100000 fue ligeramente mayor que para N=10000. La convergencia no es monótona en realizaciones individuales.

## Comparación local/cuántica y análisis estadístico N=100 000

| Magnitud | Resultado |
|---|---:|
| E_Q(a,b) | -0.70614 |
| E_Q(a,b') | +0.70828 |
| E_Q(a',b) | -0.70784 |
| E_Q(a',b') | -0.70772 |
| S_Q | -2.82998 |
| |S_L| | 2.00020 |
| σ_S | 0.00447 |
| IC aproximado 95 % para |S| | [2.8212, 2.8387] |

**Nota:** |S_L|=2.00020 es una estimación muestral y puede superar ligeramente 2 sin que el modelo local viole la cota teórica. Cambiar el texto que diga que el resultado local 'permaneció por debajo' o que no puede superar 2 en muestras finitas.

## Visibilidad

| V | |S| simulado |
|---:|---:|
| 0.70 | 1.97348 |
| 1.00 | 2.83316 |

Sustituir los valores anteriores 1.98522 y 2.82692. La simulación evalúa nueve visibilidades **no equiespaciadas** entre 0.50 y 1.00; cambiar la frase si se entendía que eran equidistantes.

## Otras tareas del reporte

- Incorporar y citar una figura reproducida del artículo científico original (no incluida en este ZIP).
- Verificar números de ensayos y su definición exacta en Delft/Viena/NIST con los artículos.
- Eliminar comentarios `% Pendiente` del LaTeX.
- Revisar que la sección de uso de IA concuerde con el trabajo efectivamente realizado.
