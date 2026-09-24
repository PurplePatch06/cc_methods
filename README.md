# Códigos de Cadena de Freeman: F4 y F8

## Descripción

Este repositorio contiene dos implementaciones para obtener el contorno de una figura mediante el **Código de Cadena de Freeman**.

Se implementan dos métodos:

* **F4:** utiliza conectividad de 4 direcciones.
* **F8:** utiliza conectividad de 8 direcciones.

Las implementaciones reciben imágenes y recorren los píxeles que forman el contorno de la figura para generar su correspondiente cadena de direcciones.

## Archivos

### `F4.ipynb`

Implementación del Código de Cadena de Freeman utilizando **conectividad F4**.

En este método se consideran los cuatro vecinos ortogonales de cada píxel:

```text
    1
    ↑
2 ← ● → 0
    ↓
    3
```

### `F8.ipynb`

Implementación del Código de Cadena de Freeman utilizando **conectividad F8**.

En este método se consideran los ocho vecinos alrededor de cada píxel:

```text
3  2  1
 \ | /
4--●--0
 / | \
5  6  7
```

Esto permite representar desplazamientos horizontales, verticales y diagonales.

## Imágenes

Las imágenes utilizadas como entrada se encuentran en la carpeta `images/`.

Entre las imágenes incluidas se encuentran:

* `Glas-1.gif`
* `fly-1.gif`
* `horse-1.gif`
* `cow.png`
* `horse.png`
* `stef-01.gif`

## Funcionamiento general

Ambas implementaciones siguen un proceso similar:

1. Cargar la imagen.
2. Procesar la imagen para obtener la información necesaria para identificar la figura.
3. Identificar un punto inicial del contorno.
4. Recorrer el contorno de acuerdo con la conectividad correspondiente.
5. Registrar las direcciones de desplazamiento.
6. Generar la cadena de Freeman resultante.

La diferencia principal entre ambos métodos es el número de direcciones que pueden utilizarse durante el recorrido del contorno.

## Ejecución

Los archivos `.ipynb` pueden abrirse utilizando:

* Jupyter Notebook
* JupyterLab
* Visual Studio Code

Las imágenes necesarias para las pruebas se encuentran en la carpeta `images/`.

## Estructura del repositorio

```text
cc_methods/
│
├── README.md
├── F4.ipynb
├── F8.ipynb
└── images/
    ├── Glas-1.gif
    ├── cow.png
    ├── fly-1.gif
    ├── horse-1.gif
    ├── horse.png
    └── stef-01.gif
```

## Autor

**Gael Guzmán Solís**

Ingeniería en Computación Inteligente
Universidad Autónoma de Aguascalientes
