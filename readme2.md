# Diseño y Construcción de Solenoide de Núcleo de Aire (719 nH)

Este documento detalla los parámetros de construcción y la justificación matemática para la fabricación manual de un solenoide
con una inductancia objetivo de 719 nH.

## 1. Parámetros Físicos Finales

Tras el proceso de ajuste mecánico, las dimensiones definitivas de la bobina son:

* **Diámetro total externo:** 13.9 mm
* **Calibre del alambre de cobre ($d$):** 1 mm
* **Diámetro efectivo ($D$):** 12.9 mm (Medido de centro a centro del alambre).
* **Número de vueltas ($N$):** 15
* **Longitud total del solenoide ($l$):** 45.5 mm
* **Material del núcleo:** Aire ($\mu_r \approx 1$)

## 2. Comparativa de Ecuaciones para el Cálculo de Inductancia

Para validar la construcción, se evaluaron dos modelos matemáticos: la ecuación del solenoide ideal y la aproximación empírica de Wheeler.

### Modelo A: Ecuación del Solenoide Ideal

Esta es la fórmula fundamental del electromagnetismo, la cual asume un solenoide de longitud infinita donde el campo magnético interior es completamente uniforme y no hay pérdidas en los extremos (efecto de bordes).

$$L = \frac{\mu_0 \cdot N^2 \cdot A}{l}$$

Donde:

* $\mu_0 = 4\pi \times 10^{-7}\text{ H/m}$ (Permeabilidad del vacío)
* $A = \pi \cdot \left(\frac{D}{2}\right)^2 = \pi \cdot \left(\frac{0.01265\text{ m}}{2}\right)^2 \approx 1.2568 \times 10^{-4}\text{ m}^2$
* $l = 0.0436\text{ m}$

### Modelo B: Fórmula de Wheeler (Ecuación Utilizada)

Harold A. Wheeler desarrolló esta fórmula empírica en 1928, optimizada para solenoides de una sola capa en radiofrecuencia. Está adaptada para ingresar los valores directamente en milímetros y devolver el resultado en microhenrios ($\mu$H).

$$L= \frac{D^2 \cdot N^2}{25.4 \cdot (18D + 40l)}$$

Donde $D$ y $l$ se ingresan en milímetros.

---

## 3. Sustitución de Valores y Resultados

Al reemplazar nuestros parámetros físicos de construcción en ambos modelos, obtenemos una diferencia notable:

**Cálculo con Solenoide Ideal:**


$$L_{ideal} = \frac{(4\pi \times 10^{-7}) \cdot 15^2 \cdot (1.2568 \times 10^{-4})}{0.0436}$$

$$L_{ideal} = \frac{3.553 \times 10^{-8}}{0.0436} \approx 8.15 \times 10^{-7}\text{ H} = \mathbf{815\text{ nH}}$$

**Cálculo con Fórmula de Wheeler:**


$$L_{wheeler} = \frac{12.65^2 \cdot 15^2}{25.4 \cdot (18 \cdot 12.65 + 40 \cdot 43.6)}$$

$$L_{wheeler} = \frac{160.0225 \cdot 225}{25.4 \cdot (227.7 + 1744)}$$

$$L_{wheeler} = \frac{36005.06}{50081.18} \approx \mathbf{719\text{ nH}}$$

## 4. Justificación del Modelo Utilizado

Para el diseño de este componente, **se descartó la ecuación del solenoide ideal y se utilizó la fórmula de Wheeler.** La ecuación ideal ($L = \mu_0 N^2 A / l$) solo es precisa cuando la longitud del solenoide es, por lo menos, 10 a 20 veces mayor que su diámetro. En nuestro caso, la longitud (43.6 mm) es apenas unas 3.4 veces el diámetro (12.65 mm). En "solenoides cortos", gran parte de las líneas de campo magnético escapan por los costados entre las espiras y en los extremos, lo que reduce la inductancia real.

Como se observa en los cálculos, la ecuación ideal sobreestima el valor arrojando **815 nH**. La fórmula de Wheeler toma en cuenta esta geometría y el factor de forma, proporcionando el valor exacto de **719 nH** que fue nuestro objetivo de diseño.
