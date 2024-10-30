# Python

Hola mundo:

```py linenums="1" hl_lines="1" title="Codigo hola mundo en python, bloque resaltado"
print("Hello world!")
```

## Variables

No pueden iniciar con un numero, pero si finalizar

```py linenums="1"
variable1 = "Primer variable"
variable2 = 2
```

## Tipos de datos

### Enteros `int`

### Decimales, punto flotante `float`

### Constantes

En Python existen constantes, aunque no están explícitamente definidas como en otros lenguajes de programación. Sin embargo, Python tiene algunas convenciones y módulos que permiten trabajar con constantes de manera efectiva.

**Constantes en python:**

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
