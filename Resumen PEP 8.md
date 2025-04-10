# 🐍 Resumen PEP 8

# **Guía de estilo para escribir código Python**

---

## 🔤 Nombres (naming)

- **Funciones, variables y atributos**: usar *snake_case* → **`mi_variable`, `calcular_total()`**
- **Clases**: usar *CamelCase* → **`MiClase`, `ClientePremium`**
- **Constantes**: todo en mayúsculas con guiones bajos → **`PI`, `MAX_INTENTOS`**

📌 Ejemplo:

```python
total_final = calcular_descuento(precio, porcentaje)

class ClientePremium:
    pass

PI = 3.1416
MAX_REINTENTOS = 5
```

---

## 📏 Sangría y longitud de línea

- Usar 4 espacios por nivel de indentación (NO tabs).
- **Máximo 79 caracteres** por línea.
- **Líneas en blanco (vacías)** para separar funciones, clases y bloques lógicos.

📌 Ejemplo:

```python
# Bien
if valor > 10:
    print("Mayor a diez")

# Mal
if valor > 10: print("Mayor a diez")
```

---

## 🎨 Espaciado

- Separar operadores con espacios.
- No poner espacios innecesarios dentro de paréntesis, corchetes o llaves.

📌 Ejemplo:

```python
# Bien
x = (a + b) * c

# Mal
x=(a+b )* c
```

---

## 📚 Comentarios

- Comentarios de una línea: Usar **`#`** seguido de un espacio.
- Comentá para **explicar el por qué**, no el qué (el qué ya lo dice el código).
- Usá frases completas, empezando con mayúscula, y preferentemente en español si el equipo lo permite.

📌 Ejemplo:

```python
# Aumenta el precio un 21% por IVA
precio_final = precio * 1.21
```

---

## 🧼 Importaciones

- Un import por línea.
- Agrupar en orden:
    1. Módulos estándar de Python
    2. Módulos de terceros
    3. Módulos propios

📌 Ejemplo:

```python
import os
import sys

import requests

import mi_script
```

---

## 🧠 Organización del código

- Funciones pequeñas, con un solo propósito, que hagan **una sola cosa bien**.
- Clases bien organizadas, y sin mezclar muchas responsabilidades.
- Evitar repeticiones innecesarias → si ves algo repetido, quizás sea función.

📌 Ejemplo:

```python
# Mal
def x(y):
    return y*1.21

# Bien
def calcular_precio_con_iva(precio):
    return precio * 1.21
```

---

## 🧪 Buenas prácticas generales

- Elegí claridad antes que complejidad.
- Evitá duplicar código.
- Usá nombres significativos/descriptivos → **`total_final`** mejor que **`x`**
- No abuses del comentario tipo “por si acaso”.

---

## 🤖 Extras útiles

- Usar **`"""Docstrings"""`** en funciones.
- Herramientas que ayudan:
    - **`flake8`** (valida estilo)
    - **`black`** (formateo automático)
    - **`pylint`** (análisis completo)

Estas herramientas te ayudan a seguir la PEP 8 automáticamente.

📌 Ejemplo:

```python
def calcular_total(precio, iva=0.21):
    """Calcula el total con IVA. IVA por defecto: 21%."""
    return precio * (1 + iva)
```

Información adquirida de:

https://peps.python.org/pep-0008/