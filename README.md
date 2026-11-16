# Implementación y evaluación de filtros digitales

## Descripción del proyecto

Este proyecto corresponde a la Actividad Formativa 3: Implementación y evaluación de filtros digitales.

El objetivo es diseñar, implementar y evaluar filtros digitales pasa bajos, pasa altos y pasa bandas utilizando Python y Jupyter Notebook.

Se generó una señal compuesta por diferentes frecuencias y ruido blanco para analizar el comportamiento de los filtros y comprobar su efectividad mediante gráficas y cálculos matemáticos.

## Objetivos

- Diseñar filtros digitales utilizando el método Butterworth.
- Implementar filtros pasa bajos, pasa altos y pasa bandas.
- Analizar señales antes y después del filtrado.
- Estudiar las respuestas en frecuencia.
- Evaluar los resultados mediante RMS y la Transformada Rápida de Fourier (FFT).

## Tecnologías utilizadas

- Python
- Jupyter Notebook
- NumPy
- SciPy
- Matplotlib
- Pandas

## Parámetros de simulación

| Parámetro | Valor |
|---|---:|
| Frecuencia de muestreo | 1000 Hz |
| Duración de la señal | 2 segundos |
| Frecuencia 1 | 5 Hz |
| Frecuencia 2 | 50 Hz |
| Frecuencia 3 | 120 Hz |
| Ruido | Blanco |
| Tipo de filtro | Butterworth |
| Orden del filtro | 4 |

## Filtros implementados

### 1. Filtro pasa bajos

- Frecuencia de corte: 30 Hz.
- Conserva principalmente la frecuencia de 5 Hz.
- Atenúa las frecuencias superiores.

### 2. Filtro pasa altos

- Frecuencia de corte: 70 Hz.
- Conserva principalmente la frecuencia de 120 Hz.
- Atenúa las frecuencias inferiores.

### 3. Filtro pasa bandas

- Frecuencia inferior: 40 Hz.
- Frecuencia superior: 60 Hz.
- Conserva principalmente la frecuencia de 50 Hz.
- Atenúa las frecuencias externas al intervalo.

Para aplicar los filtros se utilizó `sosfiltfilt` de SciPy, evitando el desfase de fase en la señal filtrada.

## Resultados obtenidos

### Comparación de valores RMS

| Señal | Valor RMS |
|---|---:|
| Original | 1.3203 |
| Pasa bajos | 0.7262 |
| Pasa altos | 0.8370 |
| Pasa bandas | 0.6955 |

### Resultados del análisis FFT

| Señal | 5 Hz | 50 Hz | 120 Hz |
|---|---:|---:|---:|
| Original | 1.0122 | 0.9813 | 1.0051 |
| Pasa bajos | 1.0127 | 0.0191 | 0.0015 |
| Pasa altos | 0.0008 | 0.0586 | 0.9924 |
| Pasa bandas | 0.0034 | 0.9722 | 0.0006 |

Los resultados demuestran que cada filtro conserva principalmente la frecuencia correspondiente a su configuración y atenúa las demás componentes.

## Estructura del proyecto

```text
Filtros-Digitales/
│
├── README.md
└── Filtros_Digitales.ipynb
```

## Instalación y ejecución

1. Instalar Python.
2. Instalar Jupyter Notebook y las librerías necesarias:

```bash
pip install numpy scipy matplotlib pandas notebook
```

3. Descargar o clonar este repositorio.
4. Iniciar Jupyter Notebook:

```bash
jupyter notebook
```

5. Abrir el archivo `Filtros_Digitales.ipynb`.
6. Ejecutar las celdas en orden.

## Conclusiones

La implementación permitió comprobar el funcionamiento de los filtros digitales pasa bajos, pasa altos y pasa bandas.

Mediante las gráficas en el dominio del tiempo, las respuestas en frecuencia, los valores RMS y el análisis FFT fue posible evaluar los cambios producidos en las señales.

Los resultados demostraron que los filtros digitales son herramientas útiles para seleccionar determinadas frecuencias y reducir componentes no deseadas dentro de una señal.

## Autor

Estudiante de Ingeniería en Desarrollo de Software.

**Actividad:** Formativa 3. Implementación y evaluación de filtros digitales.
