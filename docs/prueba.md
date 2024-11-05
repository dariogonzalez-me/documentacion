# Homepage

## Pagina para pruebas

### Ejemplos

#### Codigo especifico

Some more code with the `py` at the start:

```py
import tensorflow as tf
def whatever()
```

#### Con titulo

```py title="bubble_sort.py"
def bubble_sort(items):
    for i in range(len(items)):
        for j in range(len(items) -1 -i):
            if items[j] > items[j + 1]:
                items[j], items[j +1] = items[j + 1], items[j]
```

#### Numero de linea

```py linenums="1"
def bubble_sort(items):
    for i in range(len(items)):
        for j in range(len(items) -1 -i):
            if items[j] > items[j + 1]:
                items[j], items[j +1] = items[j + 1], items[j]
```

#### Highlighting lines

```py hl_lines="2 4"
def bubble_sort(items):
    for i in range(len(items)):
        for j in range(len(items) -1 -i):
            if items[j] > items[j + 1]:
                items[j], items[j +1] = items[j + 1], items[j]
```

#### Emogis & icons

:smile:

:fontawesome-regular-face-laugh-wink:

:fontawesome-brands-twitter:{ .twitter }

:octicons-heart-fill-24:{ .heart }
