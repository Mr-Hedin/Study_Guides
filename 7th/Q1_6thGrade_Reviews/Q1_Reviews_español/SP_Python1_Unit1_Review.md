# **Revisión - Sintaxis Básica y Bucles While**

### **Parte 1: Lo que estás repasando**

* Sintaxis básica
* Variables
* Tipos de datos
* Bucles While

---

# **Parte 2: Lo que debes saber**

---

## 1. **Primero,** `Sintaxis`:

> La sintaxis es la 'gramática' del código. Incluye el `.` (punto) `"` (comillas) `()` (paréntesis) y la ortografía correcta de tus comandos.
> Al igual que en inglés, hay reglas sobre cómo se usan estos símbolos.
> Los comandos que conoces se basan en la siguiente estructura:

```python
object.method("argument")
```

* El `objeto` es "la cosa" a la que le estás diciendo a Python que haga algo, tu `objeto` ejecutará un `método` para hacer algo.
* El objeto en CodeCombat normalmente es tu `héroe`, que podría ejecutar un `método` como `moveRight()`

```python
hero.moveRight()
```

* Para ejecutar un `método`, debes separar el objeto y el método con un `.` y añadir `()` paréntesis al final de tu método; los paréntesis le dicen al `objeto` que haga algo.

```python
student.study()
```

* Los `argumentos` te permiten decirle al método cómo hacer su trabajo, van dentro de los `()` paréntesis al final de tu método.

```python
student.study("Computer Science")
```

## 2. **Después,** `Variables y Tipos de Datos`:

* Para almacenar información para más tarde, lenguajes de programación como Python usan `variables`. Funcionan como una caja en la que guardas datos.
* Una variable necesita un **nombre** y un **valor**.
* Para crear una variable simplemente escribes el nombre, un signo igual, y luego el valor.

```python
name = "value"
```

* Hay **CUATRO** tipos de datos en Python básico.
* Es MUUY importante que no los mezcles. (Podrías acabar intentando multiplicar palabras o restar Verdadero y Falso...)
* Los cuatro tipos de datos son:

> 1. `Integer` - Un número entero, como 42
> 2. `String` - Palabras dentro de comillas, como "Hola Mundo"
> 3. `Float` - Un número decimal, como 6.7
> 4. `Boolean` - Verdadero o Falso

* Las `variables` almacenan datos de estos cuatro tipos, aquí hay un ejemplo de cada tipo guardado en diferentes variables:

```python
my_integer = 42
my_string = "Hola Mundo"
my_float = 6.7
my_boolean = False
```

## 3. **Finalmente,** `Bucles While`:

* Los bucles while te permiten ejecutar tu código varias veces.
* Los bucles while tienen dos partes: la palabra clave (`while`) y la condición.
* Al final de cada bucle while debes escribir `:` (dos puntos). Esto le dice al bucle que las siguientes líneas de código indentado forman parte del bucle.
* En el ejemplo de abajo, la palabra clave `while` se usa con la `condición` (studying) para decir que mientras estés estudiando, ejecuta el comando learn().

```python
while studying:
    learn()
```

* Mientras studying sea True, el bucle while seguirá repitiéndose.

* Para la primera parte de esta clase, solo trabajaremos con bucles `while True` para mantener las cosas simples.

* Como `True` es la condición, el bucle simplemente dice **"mientras True sea True, sigue haciendo el código de abajo"**, lo cual hace que el bucle se repita para siempre ya que `True` siempre es `True`.

* Aquí está la sintaxis de un bucle `while True`:

```python
while True:
    execute_this_command()
```

---

### **Recordatorios Útiles**

* **Consejo 1:** ¡Los argumentos son opcionales! Muchas veces verás solo un objeto ejecutando un método sin nada dentro de los paréntesis.
  `hero.moveRight()` es un comando válido para mover tu personaje una vez a la derecha.
* **Consejo 2:** La ortografía importa. Mucho. ¡Si olvidas poner una letra mayúscula, el comando no se ejecutará!
* **Consejo 3:** Consejo profesional: Si no sabes qué tipo de dato está almacenado en una variable usa el comando `type()` para que te diga qué tipo es, así:

```python
type(variable_name)
```

* **Consejo 4:** después de escribir la palabra clave y la condición para tu bucle while, indenta las líneas de código que quieres que formen parte de ese bucle usando cuatro espacios o la tecla tab.

```python
while True:
    execute_this()
    and_this()
    also_this()

but_not_this()
```

---

### **Puntos Clave**

> **Sintaxis**: La sintaxis es la gramática de tu código. ¡Escribe todo correctamente y no olvides tu puntuación!

> **Variables y Tipos de Datos**: Python guarda **TODO** dentro de variables. Un nombre, un número, el saldo de tu cuenta bancaria, lo que quieras. Todo se reduce a los cuatro tipos de datos: Integer, String, Float, Boolean.

> **Bucles While**: Los bucles while te permiten repetir código. Los bucles while te permiten repetir código. Los bucles while te permiten repetir código.

---

# Parte 3: **Práctica**

---

### Problema 1: Sintaxis

* El siguiente código se supone que hace que el héroe se mueva a la derecha, pero tiene un error de sintaxis.
* Arréglalo para que funcione correctamente.

```python
hero.moveRight
```

```python


```

### Problema 2: Sintaxis de Argumentos

El siguiente código se supone que hace que un estudiante estudie Matemáticas, pero falta el argumento.
Arréglalo agregando "Math" como argumento.

```python
student.study()
```

```python


```

### **Problema 3: Variables y Tipos de Datos**

* El siguiente código se supone que guarda una cadena en la variable `greeting`, pero algo está mal.
* Arréglalo para que funcione correctamente.

```python
greeting = Hello
```

```python


```

### **Problema 4: Tipos de Datos**

El siguiente código se supone que guarda un número decimal en `price`, pero ahora mismo está usando el tipo equivocado.
Arréglalo para que `price` sea un **float** en lugar de un **integer**.

```python
price = 5
```

```python


```

### **Problema 5: Rellenar el Espacio**

Completa el código para que se ejecute *para siempre* y haga que el héroe se mueva a la izquierda.
Llena el `keyword` y la `condición` que faltan.

```python
_____ _____:
    hero.moveLeft()
```

```python


```

### **Problema 6: Bucles While**

El siguiente código se supone que hace que el bucle se ejecute para siempre, pero tiene un error de sintaxis.
Arréglalo para que funcione correctamente.

```python
while True
    hero.moveRight()
```

```python


```

### **Problema 7: Sintaxis de Bucles While**

El siguiente código se supone que sigue imprimiendo "Hola" para siempre, pero tiene un error.
Arréglalo para que funcione correctamente.

```python
while True:
print("Hello")
```

```python


```

---

# Parte 4: **Vocabulario**

---

Palabras que debes conocer

`syntax`

> La 'gramática' de tu código. Incluye ortografía, puntuación e indentación.

`object`

> La 'cosa' que realizará alguna acción, como tu `héroe`

`method`

> La acción que tu `objeto` ejecutará, como moveRight

`argument`

> La forma en la que tu `objeto` ejecuta un `método`, va entre paréntesis, como hero.moveRight(10)

`variable`

> Un lugar donde se guardan datos. Piensa en una caja con una etiqueta: la caja podría estar etiquetada como 'número' y tener un 42 dentro.

`integer`

> Un número entero, como 42

`string`

> Palabras dentro de comillas `""`, como "¡Hola!"

`float`

> Un número decimal, como 6.7

`boolean`

> Un valor Verdadero o Falso

`while True:`

> Un tipo especial de bucle while que se repite para siempre.

`keyword`

> Una palabra especial en Python que tiene un trabajo específico, como `while` o `if`

`condition`

> Usado con sentencias condicionales para determinar si algo está sucediendo (True) o si algo no está sucediendo (False).

