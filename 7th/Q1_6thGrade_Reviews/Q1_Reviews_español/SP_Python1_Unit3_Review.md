# **Repaso - Unidad 3 Operadores Matemáticos/Lógicos/De Comparación, Break/Continue, Return**

### **Parte 1: Qué estás repasando**

* Operadores Matemáticos ( +, -, \*, /, %)
* Operadores Lógicos (and, or, not)
* Operadores de Comparación ( ==, !=, <, >, <=, >=)
* Bucles - `Break` y `Continue`
* Funciones que usan `Return`

---

# **Parte 2: Lo que debes saber**

---

## 1. **Primero,** `Operadores Matemáticos`:

> Los Operadores Matemáticos son los símbolos usados en Ciencias de la Computación para hacer operaciones matemáticas. Los operadores matemáticos son:
>
> * `+` - suma
> * `-` - resta
> * `*` - multiplicación
> * `/` - división
> * `%` - módulo

* Los operadores matemáticos nos permiten escribir `expresiones` matemáticas en Python.
* Lo bueno es que las reglas matemáticas siguen siendo las mismas en Ciencias de la Computación:
* Siempre recuerda que las matemáticas siguen el `Orden de Operaciones` - o PEMDAS

> - P - Paréntesis
> - E - Exponentes
> - M - Multiplicación
> - D - División
> - A - Adición
> - S - Sustracción

* Hacer matemáticas en Python es EXTREMADAMENTE poderoso, ¡tienes una calculadora que puedes *programar* para hacer las operaciones como quieras!
* Para escribir una expresión matemática en Python, normalmente declaras una variable para guardar la respuesta

```python
answer = 1 + 1
print(answer)
```

* En el ejemplo anterior, calculamos 1 + 1 y lo guardamos en la variable `answer`, luego lo imprimimos para el usuario.
* Usando variables, podemos crear expresiones sin usar números directamente. Las variables hacen que las expresiones sean más fáciles de leer.

```python
hours = 10
dollars = 15
pay = hours * dollars
print(pay)
```

* Este ejemplo muestra cómo las variables pueden simplificar nuestras expresiones matemáticas y hacerlas más legibles. Declaramos dos variables `hours` y `dollars`, luego las multiplicamos para obtener `pay`, que nos dice cuánto ganamos después de trabajar diez horas.
* Puedes crear expresiones mucho más complejas usando paréntesis `()` con el orden de operaciones para decidir qué se calcula primero.

```python
answer = (10 + 10) * (67 - 41)
```

* El ejemplo suma primero 10 + 10, luego resta 41 de 67, y finalmente multiplica ambos resultados.

---

* Finalmente, el operador `%` módulo no es algo que hayas visto en clase de matemáticas, pero ya lo has usado.

> - El operador `%` encuentra el residuo después de dividir.

* El operador `%` toma el número a la izquierda, lo divide entre el número a la derecha y nos dice cuánto sobra después de dividir. Por ejemplo:

```python
answer0 = 10 % 2 # esto da 0, ya que 10 dividido entre 2 no tiene residuo
answer1 = 11 % 2 # esto da 1, ya que 2 cabe en 11 cinco veces con 1 sobrante
```

---

## 2. **Después,** `Operadores Lógicos` y `Operadores de Comparación`:

> Los Operadores Lógicos se pueden usar con sentencias condicionales para combinar varias condiciones, simplificando las sentencias `if`. Incluyen:
>
> * `and`
> * `or`
> * `not`

* Recuerda, las sentencias condicionales dependen de que la `condición` sea Verdadera o Falsa. Una sentencia `if` dice: "si la condición es Verdadera, ejecuta estas líneas de código".
* Los operadores lógicos nos permiten combinar múltiples condiciones. Ejemplo: ejecutar código solo si tenemos hambre *y* tenemos un sándwich:

```python
if hungry and have_sandwich:
    student.eat("sandwich")
```

* Puedes usar el operador `or` para ejecutar código si **alguna** de las condiciones es Verdadera.
* Ejemplo: quieres hacer tu tarea si tienes tarea de matemáticas **o** inglés, no solo si tienes ambas.

```python
if math_homework or english_homework:
    student.do_homework()
```

* Puedes usar el operador `not` para *invertir* la lógica. Significa hacer lo **contrario**. Ejemplo: "si no tengo tarea, salgo afuera":

```python
if not homework:
    student.go_outside()
```

---

> Los Operadores de Comparación se usan con sentencias condicionales para comprobar si ciertas condiciones son Verdaderas. Incluyen:
>
> * `==` - igual a
> * `!=` - diferente de
> * `>` - mayor que
> * `<` - menor que
> * `>=` - mayor o igual que
> * `<=` - menor o igual que

* Los `operadores de comparación` nos permiten verificar si algo es igual, mayor o menor que otra cosa. Se usan en sentencias como `if`.
* Debes tener algo en ambos lados del operador para que funcione. Ejemplo: si quieres comprobar si dos números son iguales:

```python
gold = 10
if gold == 10:
    print("¡Tienes 10 de oro!")
```

* Otros usos incluyen verificar si algo es mayor o menor que otro valor

```python
if hero.health < 200:
    hero.say("¡Necesito una poción!")
```

* Si la salud del héroe es menor que 200, dirá "¡Necesito una poción!"
* También puedes combinar operadores lógicos y de comparación para condiciones más específicas

```python
if student.grade > 80 and weather == "sunny":
    student.go_outside()
else:
    student.study()
```

---

## 3. **Finalmente,** las palabras clave `break`, `continue`, y `return`:

> La palabra clave `break` se usa en un bucle para terminarlo inmediatamente. Funciona en bucles `while` y `for`.

* Si estás escribiendo un bucle que no quieres que dure para siempre, `break` es útil.
* La palabra clave termina el bucle y pasa a la siguiente instrucción fuera del bucle

```python
while True:
    print("esto solo pasa una vez porque usamos break")
    break
```

* `break` es útil cuando quieres salir del bucle solo si pasa algo.
* Ejemplo: seguir haciendo tarea hasta terminarla:

```python
while True:
    if homework:
        do_homework:
    else:
        break
```

---

> La palabra clave `continue` se usa en un bucle para saltar a la siguiente iteración. Funciona tanto en bucles `while` como `for`.

* Si no quieres salir del bucle, pero sí saltar al siguiente paso, usa `continue`
* Esto es útil si quieres ejecutar parte del código pero no todo cuando cierta condición es Verdadera.
* Ejemplo: sumar 1 al oro cada vez que encuentres un objeto, pero no cuando no haya objeto:

```python
while True:
    item = hero.findNearestItem()
    if item:
        hero.moveXY(item.pos.x, item.pos.y)
    else:
        continue
    gold += 1
```

* `continue` se vuelve más útil en bucles complejos y en `for`.

---

> La palabra clave `return` se usa en una función cuando quieres terminarla y `devolver` algún dato.

* `return` se usa para decirle a la función que haga su trabajo y luego regrese. Puede usarse solo para terminar la función o con un valor para devolverlo.
* Ejemplo: una función que suma 10 a un número y devuelve el resultado:

```python
def add_ten(number):
    new_number = number + 10
    return new_number

add_ten(20)
```

* También puedes usar `return` sin valor para salir de una función inmediatamente

```python
def check_for_item():
    hero.findNearestItem()
    if not item:
        return
    else:
        hero.moveXY(item.pos.x, item.pos.y)
        hero.say("¡Encontré un objeto!")
```

---

### **Recordatorios útiles**

* **Tip 1:** Puedes usar operadores matemáticos en los argumentos de un comando.

```python
hero.moveXY(hero.pos.x + 10, hero.pos.y)
```

* Esto movería al héroe 10 posiciones a la derecha sin importar dónde esté.

- **Tip 2:** Revisa tus paréntesis `()` al usar operadores matemáticos. El orden de operaciones evalúa primero lo que está dentro de paréntesis.
- **Tip 3:** Asegúrate de tener condiciones completas al usar `operadores lógicos`. Ejemplo:

```python
# condición válida
if hero.gold == 100 or hero.gold == 1:
    hero.moveXY(item.pos.x, item.pos.y)

# NO es condición completa
if hero.gold == 100 or 1:
    hero.moveXY(item.pos.x, item.pos.y)
```

* **Tip 4:** Los valores devueltos por `return` se pueden guardar en variables. Ejemplo:

```python
item = hero.findNearestItem()
```

* hero.findNearestItem() tiene la palabra clave `return` en su código interno. Devuelve el objeto más cercano.

---

### **Puntos clave**

> **Expresiones Matemáticas**: Los operadores matemáticos permiten calcular expresiones en Python

> **Operadores Lógicos**: Permiten combinar condiciones en una sentencia `if`

> **Operadores de Comparación**: Permiten comparar dos valores para ver si son iguales, mayores o menores

> **break**: termina un bucle por completo

> **continue**: pasa a la siguiente iteración de un bucle

> **return**: termina una función y devuelve un valor

<br>
<br>
<br>
<br>
<br>

---

# Parte 3: **Práctica**

---

### Problema 1: Operadores Matemáticos

* El código siguiente debe sumar 10 a dollars y luego multiplicar por hours, pero el orden de operaciones es incorrecto.
* Corrígelo para que funcione correctamente.

```python
my_pay = 10 + dollars * hours
```

```python


```

### Problema 2: Operadores Matemáticos

Rellena el espacio en blanco para que el código encuentre el residuo de dos números.

```python
remainder = 100 __ 12
```

```python


```

### **Problema 3: Operadores Matemáticos**

* Evalúa la expresión y escribe el valor de `answer`

```python
answer = (((1 + 9) + (10 * 10)) / 10) / 2
```

```python


```

### **Problema 4: Operadores Lógicos**

El código debe comprobar si el estudiante tiene tarea de matemáticas, inglés o ciencias, pero algo está mal.
Corrige la sintaxis del condicional.

```python
math = False
english = True
science = False

if math and english and science:
    student.do_homework()
```

```python


```

### **Problema 5: Operadores de Comparación**

Completa el código: si la temperatura es mayor a 90, imprime "Hace mucho calor"; si es menor a 60, imprime "Hace frío"; de lo contrario, imprime "La temperatura está bien".

```python
if temperature ___ 90:
    print("Hace mucho calor")
elif temperature ___ 60:
    print("Hace frío"):
else:
    print("La temperatura está bien")
```

```python


```

### **Problema 6: break**

Termina el bucle usando `break` si el héroe encuentra un objeto.
Reescribe el código.

```python
while True:
    item = hero.findNearestItem()
    enemy = hero.findNearestEnemy()
    if item:
        items_found += 1
        hero.moveXY(item.pos.x, item.pos.y)
    else:
        hero.attack(enemy)
```

```python








`
```

### **Problema 7: continue**

Corrige la función para que solo imprima números pares. Usa `continue` para saltar los impares.

```python
while True:
    number = number + 1
    if number % 2 == 1:
        print("impar")
    else:
        print("par")
```

```python








```

### **Problema 8: Sentencias Return**

Completa los espacios para que la función devuelva la suma de dos números.

```python
def add_two_numbers(number1, number2):
    the_sum = number1 + number2
    _____ ______

answer = _____________
```

```python






```

---

# Parte 4: **Vocabulario**

---

Palabras que debes conocer

`operadores matemáticos`

> Símbolos que hacen operaciones matemáticas en código: `+`, `-`, `*`, `/`, `%`.

`suma +`

> Suma dos valores.

`resta -`

> Resta el número de la derecha al de la izquierda.

`multiplicación *`

> Multiplica dos valores.

`división /`

> Divide el número de la izquierda entre el de la derecha.

`módulo %`

> Devuelve el residuo de una división. Ejemplo: `11 % 2` es `1`

`expresión`

> Código que calcula un valor matemático (ejemplo: `hours * dollars`).

`evaluar`

> Lo que hace Python al calcular una expresión.

`operadores lógicos`

> Palabras que combinan o invierten condiciones: `and`, `or`, `not`.

`and`

> Verdadero solo si **ambas** condiciones son Verdaderas.

`or`

> Verdadero si **alguna** condición es Verdadera.

`not`

> Invierte una condición (True -> False).

`condición`

> Una sentencia que es Verdadera o Falsa.

`operadores condicionales/de comparación`

> Símbolos que comparan valores: `==`, `!=`, `>`, `<`, `>=`, `<=`.

`igual a (==)`

> Verdadero si dos valores son iguales.

`diferente (!=)`

> Verdadero si dos valores son distintos.

`mayor que >`

> Verdadero si el valor de la izquierda es mayor.

`menor que <`

> Verdadero si el valor de la izquierda es menor.

`mayor o igual >=`

> Verdadero si el valor de la izquierda es mayor **o** igual.

`menor o igual <=`

> Verdadero si el valor de la izquierda es menor **o** igual.

`break`

> Sale inmediatamente de un bucle.

`continue`

> Salta el resto de la iteración y pasa a la siguiente.

`return`

> Termina una función y devuelve un valor.

