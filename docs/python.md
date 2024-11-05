# Python

Hola mundo:

```py linenums="1" hl_lines="1" title="Codigo hola mundo en python, bloque resaltado"
print("Hello world!")
```

## Tipos de datos numéricos

* Enteros `int`:

Representan números enteros, positivos o negativos, sin decimales. Ejemplo: 1, 2, 3, etc.

* Decimales, punto flotante `float`:

Representan números decimales. Ejemplo: 3.14, -0.5, etc.

* Complejos `complex`:

Representan números complejos, con parte real e imaginaria. Ejemplo: 3 + 4j, -2 - 5j, etc.

## Tipos de datos de texto

* Cadena `str`:

Representa una secuencia de caracteres. Ejemplo: "Hola", 'Hola', etc.

## Tipos de datos de colección

* Lista `list`:

Una secuencia ordenada de elementos, que pueden ser de diferentes tipos. Ejemplo: [1, 2, 3], ["a", "b", "c"], etc.

* Tupla `tuple`:

Una secuencia ordenada e inmutable de elementos. Ejemplo: (1, 2, 3), ("a", "b", "c"), etc.

* Diccionario `dict`:

Una colección de pares clave-valor. Ejemplo: {"nombre": "Juan", "edad": 30}, etc.

* Conjunto `set`

Una colección sin orden y sin duplicados de elementos. Ejemplo: {1, 2, 3}, {"a", "b", "c"}, etc.

## Tipos de datos lógicos

* Boleano `bool`

Representa un valor verdadero o falso. Ejemplo: True, False.

## Tipos de datos especiales

* NoneType `none`

Representa la ausencia de valor.

* Bytes `bytes`

Representa una secuencia de bytes.

**Constantes:**

En Python existen constantes, aunque no están explícitamente definidas como en otros lenguajes de programación. Sin embargo, Python tiene algunas convenciones y módulos que permiten trabajar con constantes de manera efectiva.

1. numeros especiales:
    Python tiene algunas constantes numéricas especiales, como `inf` (infinito), `-inf` (menos infinito) y `nan` (no es un número), que se pueden acceder mediante el módulo *`math`*.

2. Constantes matemáticas:
    El módulo *`math`* también proporciona constantes matemáticas como `pi`, `e`, `tau`, etc.

3. Constantes de tipo:
    Python tiene constantes de tipo, como `True`, `False` y `None`, que se utilizan para representar valores booleanos y nulos.

4. Constantes definidas por el usuario:
    Aunque Python no tiene una palabra clave específica para definir constantes, se puede utilizar la convención de nombrar variables en *"mayúsculas y separarlas con guiones bajos"* para indicar que son constantes.

**Módulos para trabajar con constantes:**

1. ``enum``:
    El módulo *`enum`* permite definir enumeraciones, que pueden ser utilizadas como constantes.

    ```py linenums="1"
    from enum import Enum
    class Color(Enum):
        ROJO = 1
        VERDE = 2
        AZUL = 3
    print(Color.ROJO)  # Color.ROJO
    ```

2. `contansts`:
    El módulo *`constants`* es un paquete de terceros que permite definir constantes de manera explícita.

    ```py linenums="1"
    import constants
        constants.DEFINE_INT('MI_CONSTANTE', 42)
        print(constants.MI_CONSTANTE)  # 42
    ```

## Variables

No pueden iniciar con un numero, pero si finalizar

```py linenums="1"
variable1 = "Primer variable"
variable2 = 2
```
