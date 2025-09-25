# **Repaso - Unidad 2 Condicionales, Funciones, Eventos**

### **Parte 1: Lo que estás repasando**

* Coordenadas y Atributos
* Sentencias Condicionales
* Funciones
* Funciones con Parámetros

---

# **Parte 2: Lo que debes saber**

---

## 1. **Primero,** `Sistemas de Coordenadas`:

> Los sistemas de coordenadas usan una `x` y una `y` para especificar dónde está algo.

* Los sistemas de coordenadas no están necesariamente relacionados con Python, pero los usamos bastante en CodeCombat.

* La coordenada `x` nos dice qué tan a la izquierda o a la derecha está algo.

* La coordenada `y` nos dice qué tan arriba o abajo está algo.

* Puedes ver un ejemplo de una cuadrícula de coordenadas abajo: <br>![image.png](output_files/4e69b36c-f8db-4bda-b671-2d2077abfdb6.png)

* Para nuestros propósitos, usarás coordenadas con el comando `hero.moveXY(x,y)`
  Ejemplo:

```python
hero.moveXY(67, 42) # mueve al héroe hasta que sus coordenadas sean x=67, y=42
```

* Una forma útil de encontrar las coordenadas de algo es a través de los `atributos`, que son como variables adjuntas a un objeto.
* Los `atributos` se pueden acceder usando el `operador punto`. (Literalmente solo un punto.)
* Por ejemplo, `hero.pos` nos da una coordenada combinada de `x` y `y` de la posición actual de nuestro héroe.
* Esto también funciona con enemigos y **objetos**.
* Generalmente no queremos la `x` y la `y` combinadas, así que casi siempre obtendremos la x y luego la y de esta forma:

```python
# Primero obtenemos los valores x e y de los atributos del objeto
x = item.pos.x
y = item.pos.y

# Luego podemos usar las coordenadas del objeto para movernos hacia él, ¡NO IMPORTA DÓNDE ESTÉ! No más números, sé perezoso de la forma inteligente.
hero.moveXY(x, y)

# Yo soy perezoso, así que lo pongo todo en una sola línea - esto también es válido.
hero.moveXY(item.pos.x, item.pos.y)
```

---

## 2. **Después,** `Condicionales`:

> Las sentencias condicionales son el núcleo de la programación: Nos permiten como programadores tomar decisiones en nuestro código basadas en diferentes `condiciones`. La condicional más simple es la sentencia `if`. Aunque, los bucles `while`, `for`, y las sentencias `switch` también son tipos de condicionales ya que dependen de que alguna `condición` sea `True`.

* Las sentencias `if` nos permiten seleccionar diferentes líneas de código para ejecutar basadas en la `condición`
* Para escribir una sentencia `if`, usa la palabra clave `if` y una `condición` como en el ejemplo de abajo:

```python
if studying:
    learn_something_cool()
```

* La sentencia `if` de arriba se ejecutaría *una sola vez* solo *si* studying es `True`.
* Como puedes cambiar el valor de las variables, también puedes cambiar cuándo se ejecuta cierto código

```python
raining = False
if raining:
    student.use_umbrella()
```

* Como raining fue definido como `False`, el estudiante no usaría un paraguas en el código de arriba.

  <br>
* Las sentencias `if` no son la única forma de seleccionar qué código ejecutar, también podemos usar `elif` y `else` para controlar cuándo sucede algo.
* Las sentencias `elif` solo pueden usarse después de una sentencia `if`. Permiten decir "si la primera parte no fue True, revisa si otra cosa lo es".
* Puedes encadenar tantos `elif` como quieras después de un `if`.
* Ejemplo de `elif`:

```python
math_homework = False
english_homework = True
if math_homework:
    student.calculate()
elif english_homework:
    student.write_essay()
```

* Nota que tanto `if` como `elif` requieren dos puntos `:` después de la condición y sangría en las líneas que les pertenecen.
* En el ejemplo de arriba, el estudiante no tiene math\_homework, pero sí tiene english\_homework, entonces no quiere hacer matemáticas si no tiene tarea de matemáticas que hacer, así que el código revisa ambas tareas usando `if` y `elif`.

  <br>
* Finalmente, tenemos la sentencia `else` que debe usarse **al final** en un bloque `if`.
* `else` dice "si nada de lo anterior es True, haz esto en su lugar".
* Por ejemplo:

```python
if homework:
    student.do_homework()
else:
    run_in_circles()
```

* `if`, `elif` y `else` se usan juntos para darnos *tantas* opciones como queramos, ejecutando código solo *si* algo es True.

```python
if raining:
    student.wear("coat")
elif hungry:
    student.eat("food")
elif homework:
    student.eat("homework")
else:
    student.stare("wall")
```

## 3. **Finalmente,** `Funciones`:

> Las `Funciones` son listas de comandos. Funcionan igual que una receta para cocinar algo. Una función te permite agrupar un **montón** de código en un solo comando y reutilizarlo tantas veces como quieras.

* Una función necesita ser `definida` antes de poder usarse.
* Para `definir` una función, usa la palabra clave `def`, el nombre de la función, un conjunto de paréntesis `()` y dos puntos `:`.
* Luego, indenta las líneas de código que quieras que se ejecuten cada vez que corras la función.
* Ejemplo:

```python
def make_sandwich():
    student.get("bread", 2)
    student.get("peanut_butter")
    student.get("jelly")
    student.get("knife")
    student.spread("peanut butter")
    student.spread("jelly")
    student.eat("sandwich")
```

* Ahora que hemos escrito todas esas líneas de código, podemos `llamar` la `función` para que haga algo.
* ¡Las `Funciones` NO hacen NADA hasta que se `llaman`!
* Para `llamar` una función, simplemente escribe el nombre de la función seguido de paréntesis `()`

```python
make_sandwich()
```

* Esto haría que todas las líneas de código que definimos anteriormente se ejecuten.
* Las funciones son **extremadamente** útiles ya que podemos `llamarlas` tantas veces como queramos. En lugar de escribir 7 líneas de código cada vez que quieras un sándwich, puedes simplemente llamar `make_sandwich` una y otra vez hasta llenarte.

  <br>
* Última cosa sobre funciones:
* Si necesitas escribir una función pero quieres poder personalizar lo que pasa dentro cuando la `llames`, puedes usar un tipo especial de `variable` llamada `parámetro`.
* Los `parámetros` nos permiten pasar `argumentos` a una función *cuando la llamamos*.
* Para crear una función con un `parámetro` simplemente escribe el nombre del parámetro dentro de los paréntesis al definir la función.
* Por ejemplo, si quisieras crear una función que diga "Hola" y el nombre de alguien, podrías usar un parámetro para cambiar el nombre cada vez que la llames.

```python
def greet_person(name):
    print("Hello")
    print(name)

greet_person("Mr. Hedin")
greet_person("Mrs. Kitchens")
```

* La función de arriba nos permite cambiar el parámetro `name` cada vez que la llamamos, ¡dando un resultado diferente cada vez!

---

### **Recordatorios Útiles**

* **Consejo 1:** Si no estás seguro de dónde estará un objeto, usa item.pos.x y item.pos.y para que tu héroe lo descubra cuando lo vea.
* **Consejo 2:** Puedes encadenar cualquier número de sentencias `elif` - lo que significa que tienes opciones **ilimitadas**.
* **Consejo 3:** Las sentencias `if` solo se ejecutan **una vez**, si necesitas repetir un `if`, podrías querer usar un bucle.

```python
while homework:
    if math_homework:
        calculate()
    elif english_homework:
        write()
```

* **Consejo 4:** Puedes poner una sentencia if dentro de otra if para `anidar` tu condicional. Básicamente, esto te permite verificar si más de una cosa es True al mismo tiempo.

```python
if no_homework:
    if sunny:
        go_outside()
```

* **Consejo 5:** Puedes definir funciones y luego llamarlas dentro de otra función.

```python
def do_math():
    calculate()

def do_english():
    write()

def do_homework():
    do_math()
    do_english()

do_homework()
```

---

### **Conclusiones Clave**

> **Coordenadas**: Las coordenadas permiten que el héroe en CodeCombat se mueva a una posición x,y

> **Atributos**: Los atributos son como variables almacenadas en un objeto. Como hero.health que guarda tu salud actual.

> **Condicionales (if, elif, else)**: `if` nos deja ejecutar código solo *si* algo es True. `elif` hace lo mismo pero solo si lo primero no fue True. `else` dice "si nada de lo anterior fue True, ejecuta estas líneas".

> **Funciones**: Las funciones son listas de otros comandos que se pueden ejecutar todos juntos cada vez que se llaman. Limpian tu código y son reutilizables, ¡así no tienes que escribir tantas líneas!

> **Parámetros**: Permiten personalizar tus funciones cuando las llamas. Pueden hacer que tu código reutilizable sea personalizable *cada vez* que lo uses.

---

# Parte 3: **Práctica**

---

### Problema 1: Coordenadas

* El código de abajo se supone que debe mover al héroe a (42, 67)
* Arréglalo para que funcione correctamente.

```python
hero.moveXY(x,y)
```

```python
```

### Problema 2: Coordenadas

El código de abajo se supone que debe hacer que el héroe se mueva al objeto más cercano.
Arréglalo agregando el atributo `x` y `y` del objeto como argumentos.

```python
while hero.gold < 20:
    item = hero.findNearestItem()
    if item:
        hero.moveXY(___.___.___, ___.___.___)
```

```python
```

### **Problema 3: Condicionales**

* El código de abajo se supone que debe hacer que el estudiante use un paraguas si está lloviendo, pero algo está mal.
* Arréglalo para que funcione correctamente.

```python
raining = True
if umbrella:
    raining()
```

```python
```

### **Problema 4: Condicionales**

El código de abajo se supone que debe verificar si el estudiante tiene tarea de matemáticas, inglés o ciencias, y luego hacerla, pero algo está mal.
Arréglalo para que la sintaxis condicional verifique cada condición correctamente.

```python
math = False
english = True
science = False

elif math
    do_math()
if english
    do_english()
else:
    do_science()
```

```python
```

### **Problema 5: Condicionales**

Completa el código para que la sentencia condicional diga: si está lloviendo - usa un abrigo, si no, si está soleado - usa un sombrero, de lo contrario usa botas de nieve.

```python
_____ _____:
    student.wear("coat")
_____ _____:
    student.wear("hat")
_____:
    student.wear("snow boots")
```

```python
```

### **Problema 6: Funciones**

El código de abajo se supone que debe hornear un pastel llamando a la función `bake_cake()`.
Arréglalo para que funcione correctamente.

```python
def bake_cake():
    get("flour", 2)
    get("sugar", 1)
    get("butter", .5)
    get("eggs", 3)
    get("milk", 1)
    get("baking powder", .2)
    get("vanilla extract", .1)

    preheat("oven", 350)

    bowl.add("butter", "sugar")
    eggs.crack()
    bowl.add("eggs")
    bowl.add("vanilla extract")
    bowl.add("flour")
    bowl.add("baking powder")
    bowl.add("milk")
    bowl.mix(bowl.contents)

    pan = grease("cake pan")
    pan.add(bowl.contents.batter)

    bake(pan, 35)

    pan.cool(10)
```

```python
```

### **Problema 7: Funciones**

Completa la definición de la función de abajo para que haga que un estudiante inicie sesión en su chromebook.
Escribe al menos cuatro comandos

```python
def get_ready():
    student.open("chromebook")
    ___.___()
    ___.___()
    ___.___()
    ... # más comandos si lo crees necesario
```

```python
`








`
```

### **Problema 8: Funciones con parámetros**

La función de abajo se supone que debe saludar a cada maestro en el pasillo, pero solo saluda a uno.
Arréglala para que salude a todos los maestros que se le pasen como argumentos.

```python
def say_hello(teacher):
    print("Hello")
    print("Mr. Hedin")
    print("How are you today?")

# Esta parte está correcta... no reescribas todo aquí abajo.
say_hello("Mrs. Brock")
say_hello("Mrs. Jacobson")
say_hello("Ms. Spencer")
say_hello("Mrs. Jenkins")
say_hello("Mr. Graves")
say_hello("Ms. Lunt")
say_hello("Mr. Anderson")
say_hello("Mr. Clifford")
say_hello("Mr. Herrington")
```

```python
`








`
```

### **Problema 9: Funciones con parámetros**

Reescribe la función de abajo con un parámetro para que la función imprima el nombre de un estudiante basado en el argumento pasado cuando la llames.

```python
def say_hello():
    print("Hello")
    print("Human")
    print("How are you today?")

say_hello("escribe el nombre de alguien aquí")
say_hello("escribe el nombre de alguien aquí")
```

```python
`








`
```

---

# Parte 4: **Vocabulario**

---

Palabras que debes conocer

`coordinate system`

> Un mapa que usa un número `x` (izquierda/derecha) y `y` (arriba/abajo) para decirte dónde está algo.

`x coordinate`

> El número que muestra qué tan a la izquierda o a la derecha está algo.

`y coordinate`

> El número que muestra qué tan arriba o abajo está algo.

`attribute`

> Una pieza de información sobre un objeto, como `hero.pos` o `enemy.health`.

`dot operator`

> El punto (`.`) usado para ver el atributo de un objeto, como `item.pos.x`.

`conditional`

> Una forma de que el código tome decisiones basadas en si algo es True o False.

`if statement`

> Ejecuta código solo si una condición es True.

`elif statement`

> Significa “else if”. Revisa otra condición si el primer `if` no fue True.

`else statement`

> Ejecuta código si ninguno de los `if` o `elif` fue True.

`function`

> Un conjunto de comandos agrupados, como una receta que puedes reutilizar.

`def`

> La palabra clave usada para definir (crear) una función.

`call`

> Ejecutar una función escribiendo su nombre seguido de `()`.

`parameter`

> Una variable dentro de los paréntesis de una función que te permite personalizar lo que hace.

`argument`

> El valor real que das a un parámetro cuando llamas a la función.

---

```python
```
