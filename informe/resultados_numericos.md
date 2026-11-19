# Resultados numéricos

Los valores de esta sección corresponden a la ejecución del notebook `01_simulacion_bell.ipynb`, con semilla base 42. Se emplean generadores independientes en cada sección.

## Parámetro CHSH

Para las orientaciones $a=0°$, $a'=90°$, $b=45°$ y $b'=135°$, se utiliza

$$S=E(a,b)-E(a,b')+E(a',b)+E(a',b').$$

Con 10 000 pares por combinación se obtuvieron las siguientes correlaciones:

| Correlación | Valor |
|---|---:|
| $E(a,b)$ | -0.7064 |
| $E(a,b')$ | +0.6930 |
| $E(a',b)$ | -0.7134 |
| $E(a',b')$ | -0.7028 |

El resultado fue $S=-2.8156$, con $|S|=2.8156$.

## Tamaño de muestra

| Pares por combinación | $|S|$ | Error absoluto respecto a $2\sqrt{2}$ |
|---:|---:|---:|
| 100 | 2.8400 | 0.0116 |
| 1 000 | 2.8420 | 0.0136 |
| 10 000 | 2.8300 | 0.0016 |
| 100 000 | 2.8303 | 0.0019 |

El error no disminuye de manera estrictamente monótona en una sola realización, debido a las fluctuaciones del muestreo.

## Comparación cuántica y local

Con 100 000 pares por combinación, el modelo cuántico produjo:

| Correlación | Valor |
|---|---:|
| $E_Q(a,b)$ | -0.70614 |
| $E_Q(a,b')$ | +0.70828 |
| $E_Q(a',b)$ | -0.70784 |
| $E_Q(a',b')$ | -0.70772 |

Se obtuvo $S_Q=-2.82998$ y $|S_L|=2.00020$ para el modelo local. El pequeño exceso muestral del valor local respecto a 2 no representa una violación del límite teórico.

El error estándar estimado para el resultado cuántico fue $\sigma_S\approx0.00447$, con un intervalo aproximado del 95 % para $|S|$ de $[2.8212,2.8387]$.

## Visibilidad

Con 100 000 pares por combinación se obtuvo $|S|=1.97348$ para $V=0.70$ y $|S|=2.83316$ para $V=1.00$. El valor teórico es $|S_V|=2\sqrt{2}V$, por lo que la violación requiere $V>1/\sqrt{2}$.

## Eficiencia de detección

Las pérdidas se modelaron de manera independiente en ambos detectores. La fracción esperada de coincidencias es $\eta^2$. Las correlaciones calculadas únicamente con coincidencias pueden mantenerse cercanas al valor cuántico ideal, pero esa selección no constituye una prueba libre de la laguna de detección.
