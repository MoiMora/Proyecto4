---

## Universidad de Costa Rica
### Escuela de Ingeniería Eléctrica
#### IE0405 - Modelos Probabilísticos de Señales y Sistemas

Segundo semestre del 2020

---

* Estudiante: **Moisés Mora Ceciliano**
* Carné: **B75036**
* Grupo: **1**

---

Las funciones que se utilizan en la simuación del sistema son:

1. `fuente_info(imagen)`: Extrae en un `array` de NumPy los pixeles contenidos en la imagen.
* `rgb_a_bit(vector_pixel)`: Convierte los pixeles del 'array' de NumPy en una cadena `bits_Tx` continua de tamaño $(1 \times k)$, en donde $k$ es la cantidad total de bits de la imagen.
* `modulador_I(bits_Rx, fc, MPP)`: Convierte la señal de información (arreglo de `bits_Tx`) en una señal modulada_I bajo un esquema **QPSK**.
* `modulador_Q(bits_Rx, fc, MPP)`: Convierte la señal de información (arreglo de `bits_Tx`) en una señal modulada_I bajo un esquema **QPSK**.
* `canal_ruidoso(senal_Tx, Pm, SNR)`: Simula un canala ruidoso con **AWGN** par la `senal_Tx`.
* `demodulador(senal_Rx, portadora_I, portadora_Q, MPP)`: Demodula a `senal_Rx` (señal recibida) y determina los bits recibidos usando el criterio de demodulación por detección de energía.
* `bits_a_rgb(bits_Rx, dimensiones)`: Reconstruye los bits recibidos en `bits_Rx` en una imagen.

Las bibliotecas de Python de interés para este proyecto son:

```python
# Para manipular imágenes (Python Imaging Library)
from PIL import Image

# Para manipular 'arrays' de pixeles y bits, señales y operaciones
import numpy as np

# Para visualizar imágenes y señales
import matplotlib.pyplot as plt

# Para medir el tiempo de simulación
import time
```
