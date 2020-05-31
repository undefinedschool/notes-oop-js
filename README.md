# ![Programación Orientada a Objetos en JavaScript](https://i.imgur.com/DGCDw5r.png)

<div align="center">  
  <p align="center">
  <sub>Hola! Soy Nico (<strong>nhsz</strong>), <strong>Dev Full Stack JavaScript y mentor</strong>.</sub>
  </p>
  
  <p align="center">
    <sub>
      Hace un tiempo (principios de 2019) empecé un proyecto llamado <a href="https://undefinedschool.io"><strong>undefined school</strong></a>, una <strong>escuela de Desarrollo Web Full Stack JavaScript</strong>, 100% Open Source, con mentorías personalizadas para grupos reducidos y el foco puesto en los <strong>fundamentos</strong> y <strong>conceptos avanzados</strong>.
    </sub>
  </p>

  <p align="center">
    <sub>
      Me interesa mucho la intersección entre la educación y la tecnología, por eso también participo en proyectos como <a href="https://freecodecampba.org">freeCodeCampBA</a> (co-founder y co-organizador) y <a href="https://twitter.com/LXBA_">Learning Experience BA</a> (co-founder y co-organizador).
    </sub>
  </p>

 <p align="center">
    <sub>
  👉 Si estás arrancando en el mundo del desarrollo web y necesitás una mano, podés encontrarme en <a href="https://twitter.com/_nhsz/">Twitter</a> (también para hablar sobre cualquier tema relacionado a JavaScript o <em>#nerdeadas</em> en general 😛).
  </sub>
  </p>
  
  <p align="center">
  <sub>
    Por último, te cuento que soy muy fan del café (obvio que negro y sin azúcar), asi que si las notas te resultaron útiles y querés colaborar para que no me quede dormido y siga escribiendo guías, apuntes y más <strong>contenido Open Source en español</strong>, podés invitarme uno, gracias! ❤️
  </sub>
  </p>
  
  <p align="center">
  ☕
  <code> 
  <a href="https://cafecito.app/nhsz">
    <strong>Invitame 1 café!</strong>
  </a>
  </code>
  </p>
  <hr>
</div>

👉 Ver [todas las notas](https://github.com/undefinedschool/notes)

## Contenido

- [Objetos](https://github.com/undefinedschool/oop-js/blob/master/README.md#objetos)
  - [Sintaxis](https://github.com/undefinedschool/oop-js/blob/master/README.md#sintaxis)
- [POO](https://github.com/undefinedschool/oop-js/blob/master/README.md#poo)
- [Prototype](https://github.com/undefinedschool/oop-js/blob/master/README.md#prototype)
  - [Herencia basada en prototipos (_Prototypal Inheritance_)](https://github.com/undefinedschool/oop-js/blob/master/README.md#herencia-basada-en-prototipos-prototypal-inheritance)
  - [Otro ejemplo de herencia basada en prototipos](https://github.com/undefinedschool/oop-js/blob/master/README.md#otro-ejemplo-de-herencia-basada-en-prototipos)
- [Las funciones son funciones... y objetos
](https://github.com/undefinedschool/oop-js/blob/master/README.md#las-funciones-son-funciones-y-objetos)
- [_Factory Function_ vs `constructor`](https://github.com/undefinedschool/oop-js/blob/master/README.md#factory-function-vs-constructor)
  - [Combo función-objeto](https://github.com/undefinedschool/oop-js/blob/master/README.md#combo-funci%C3%B3n-objeto)
- [`isPrototypeOf`, `getPrototypeOf` e `instanceof`](https://github.com/undefinedschool/oop-js/blob/master/README.md#isprototypeof-getprototypeof-e-instanceof)
- [Creación de objetos](https://github.com/undefinedschool/oop-js#creaci%C3%B3n-de-objetos)
  - [`Object.create`](https://github.com/undefinedschool/oop-js/blob/master/README.md#objectcreate)
  - [`new` keyword](https://github.com/undefinedschool/oop-js/blob/master/README.md#new-keyword)
    - [`new` behind the scenes](https://github.com/undefinedschool/oop-js/blob/master/README.md#new-behind-the-scenes)
  - [`new` vs `Object.create`](https://github.com/undefinedschool/oop-js/blob/master/README.md#new-vs-objectcreate)
- [`bind`](https://github.com/undefinedschool/oop-js/blob/master/README.md#bind)
- [El problema que tenemos al usar `this`](https://github.com/undefinedschool/oop-js/blob/master/README.md#el-problema-que-tenemos-al-usar-this)
  - [Cómo forzar el valor de `this`](https://github.com/undefinedschool/oop-js/blob/master/README.md#c%C3%B3mo-forzar-el-valor-de-this)
  - [tl;dr Cómo saber el valor de `this`](https://github.com/undefinedschool/oop-js/blob/master/README.md#tldr-c%C3%B3mo-saber-el-valor-de-this)
    - [`this` es...](https://github.com/undefinedschool/oop-js/blob/master/README.md#this-es)
    - [El valor de `this` depende de varios factores...](https://github.com/undefinedschool/oop-js/blob/master/README.md#el-valor-de-this-depende-de-varios-factores)
    - [_Modos_](https://github.com/undefinedschool/oop-js/blob/master/README.md#star-modos)
  - [:warning: Ojo con `this`, los métodos y las _arrow functions_!](https://github.com/undefinedschool/oop-js/blob/master/README.md#warning-ojo-con-this-los-m%C3%A9todos-y-las-arrow-functions)
- [`Class`](https://github.com/undefinedschool/oop-js/blob/master/README.md#class)
  - [Herencia con `Class`](https://github.com/undefinedschool/oop-js/blob/master/README.md#herencia-con-class)
  - [`Class` behind the scenes](https://github.com/undefinedschool/oop-js/blob/master/README.md#class-behind-the-scenes)
- [Polimorfismo](https://github.com/undefinedschool/oop-js/blob/master/README.md#polimorfismo)
  - [Usando prototipos](https://github.com/undefinedschool/oop-js/blob/master/README.md#usando-prototipos)
  - [Usando `Class`](https://github.com/undefinedschool/oop-js/blob/master/README.md#usando--class)
- [_Getters_ & _Setters_](https://github.com/undefinedschool/oop-js/blob/master/README.md#getters--setters)
- [Métodos _estáticos_](https://github.com/undefinedschool/oop-js/blob/master/README.md#m%C3%A9todos-est%C3%A1ticos)
- [POO: Conceptos fundamentales explicados brevemente](https://github.com/undefinedschool/oop-js/blob/master/README.md#poo-conceptos-fundamentales-explicados-brevemente)
- [:fireworks: Bonus](https://github.com/undefinedschool/oop-js/blob/master/README.md#fireworks-bonus)
  - [:question: Cómo hacemos para iterar sobre las propiedades de un objeto?](https://github.com/undefinedschool/oop-js/blob/master/README.md#question-c%C3%B3mo-hacemos-para-iterar-sobre-las-propiedades-de-un-objeto)
  - [:question: Cómo hacemos para clonar un objeto?](https://github.com/undefinedschool/oop-js/blob/master/README.md#question-c%C3%B3mo-hacemos-para-clonar-un-objeto)
- [Para seguir aprendiendo...](https://github.com/undefinedschool/oop-js/blob/master/README.md#para-seguir-aprendiendo)
- [📚 Libros recomendados sobre OOP en JS](https://github.com/undefinedschool/oop-js/#-libros-recomendados-sobre-oop-en-js)
- [Conclusión](https://github.com/undefinedschool/oop-js/blob/master/README.md#conclusi%C3%B3n)

```js
// 1
const ballXPosition = 20;
const ballYPosition = 40;
const ballColor = 'red';
const ballSize = 2;

// 2
const ball = {
  xPosition: 20,
  yPosition: 40,
  color: 'red',
  size: 2
};

// 3
const ball = {
  position: {
    x: 20,
    y: 40
  },
  color: 'red',
  size: 2
};
```

- Usando notación de _ES6_ para los métodos, se puede simplificar un poco

```js
const userOne = {
  email: "ryu@ninjas.com",
  name: "Ryu",
  login() {
    console.log(`${this.email} has logged in!`)
  }
};
```

- Si tenemos una serie de variables/constantes y funciones relacionadas, podemos pensar que quizás nos convenga agruparlas, combinarlas de alguna forma, en una unidad. 
- Podemos agruparlas en una unidad que conocemos como _objeto_
- Vamos a llamar _propiedades_ a estas variables/constantes y _métodos_ a las funciones

> :star: un objeto es una colección de datos/funcionalidades relacionados (variables y funciones), que llamamos _propiedades_ y _métodos_ cuando se encuentran dentro de un objeto

## Objetos

- Un _objeto_ es una _entidad_ que tiene _propiedades_
- Si una de estas propiedades define _comportamiento_ o funcionalidad, la conocemos como _método_

```js
const array = [1, 2, 3];

array.length            // length property
array.map(x => z ** 2); // map method
```

- Las **propiedades** definen características propias de un objeto
- Los **métodos** definen comportamientos propios de un objeto
- Para acceder a una propiedad o método de un objeto, podemos utilizar: 
  - _dot notation_: `object.propertyName`, `object.methodName()`
    - **Debe ser el nombre literal de la propiedad**
  - _bracket notation_: `object['propertyName']`, `object['methodName']` 
    - **La expresión entre `[]` se evalúa para obtener el nombre de la propiedad. La utilizamos cuando la propiedad es dinámica, es decir, puede variar. Ejemplo, cuando iteramos con un `for.. in`**
  - Para crear propiedades que no tengan un nombre válido en JS, usamos strings. Ej: `'full name': Homero J. Simpson`
- Para chequear si un objeto tiene una propiedad determinada, usamos el método [`hasOwnProperty()`](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Object/hasOwnProperty) (todos los objetos lo tienen)
  - También podemos usar el operador `in`, que recibe como _string_ el nombre de la propiedad y retorna `true` si esta existe en el objeto. Ej: `console.log('length' in [])`

### Sintaxis

#### Objects literals

```js 
const obj = {};  // empty object

const myCar = {
  make: "Ford",
  model: "Mustang"
}
```

### new Object()

```js
const obj = new Object();  // empty object 

const myCar = new Object();
myCar.make = "Ford";
myCar.model = "Mustang";
```

- Son equivalentes

## POO

- _Programación Orientada a Objetos_ es un _paradigma de programación_ que utiliza _objetos_ para modelar _entidades_ del mundo real
- Los objetos son el centro del _Paradigma Orientado a Objetos_, mejor conocido como _POO_ (_OOP_ en inglés)
- JavaScript no sigue el paradigma más 'tradicional' de objetos, basado en clases, sino el basado en prototipos, aka _objetos sin clases_

> :star: Un paradigma de programación es cualquier enfoque sistemático que tomamos para intentar controlar la complejidad de nuestro código, haciendo que sea más fácil de entender y razonar (brinda estructura), mantener, modificar y extender (agregar features, funcionalidad)

![](https://2.bp.blogspot.com/-Lf_JArk4ojs/WKdrlFDWyeI/AAAAAAABE3E/PZnZbYwyDUAYqMcdG7ydgdY36BeMv-qKQCPcB/s1600/characterart-teletubbies-587f6f587b40a.png)

```js
const aTeletubbie = {
  name: 'Po',
  color: '#ff0000',
  currentPosition: 0,
  goForward: function() {
    this.currentPosition += 1;
  },
  goForwardUsingScooter: function() {
    this.currentPosition += 2;
  },
  goBack: function() {
    this.currentPosition -= 1;
  }
}

aTeletubbie.name;
aTeletubbie.color;
aTeletubbie.currentPosition;
aTeletubbie.goForward();
aTeletubbie.currentPosition;
```

- Un _paradigma de programación_ es un marco conceptual (_framework mental_), un conjunto de ideas que describe y setea una forma de entender cómo construimos y desarrollamos software.

> :star: **Tener nociones de estos paradigmas nos va a ayudar a entender mejor las herramientas que utilizamos**

![](https://i.imgur.com/INMK9IM.png)

## Prototype

- :warning: **Problema:** las propiedades pueden tomar valores únicos, pero en el caso de los métodos, estamos repitiendo las mismas funciones una y otra vez, para cada objeto (y rompiendo el principio _DRY_).

- **Solución:** mover los métodos a otro objeto (único) y que el intérprete, en el caso de que no los encuentre en los objetos anteriores, los busque en este otro

```js
const cat = {
  sound: 'meow!'
}

cat.talk();
```

```js
const cat = {
  sound: 'meow!'
}

const animal = {
  talk() {
    console.log(this.sound);
  }
}

Object.setPrototypeOf(cat, animal);
cat.talk();
```

> :star: En JS, utilizamos _prototipos_ para delegar características (propiedades) y comportamiento (métodos) a otros objetos

- Las propiedades _propias_ de un objeto (es decir, las que están definidas en él) tienen precedencia sobre las propiedades de su prototipo que tengan el mismo nombre
- El prototipo de un objeto actúa como _fallback_: si JS no encuentra una propiedad en un objeto, va a buscarla a su prototipo y sino al prototipo del prototipo, etc
  - Esto se conoce como _Prototype Chain_
  - Esta cadena termina con el prototipo de `Object`, `Object.prototype`, que es `null`, porque `null` no es un objeto y por lo tanto no puede tener una propiedad `__proto__`
- Podemos utilizar el método `hasOwnProperty()` para diferenciar entre las propiedades propias de un objeto de las propiedades que hereda de su prototipo (`in` en cambio nos dice si una propiedad pertenece a la cadena de prototipos de un objeto)
- Podemos _aumentar_ o _extender_ el prototipo de una función constructora (ó [_Factory Function_](https://www.theodinproject.com/courses/javascript/lessons/factory-functions-and-the-module-pattern?ref=lnav)) ya existente modificando su propiedad `prototype` y todos los objetos creados con esta función tendrán las nuevas propiedades

```js
function Dog() {}

Dog.prototype.breed = 'Bulldog';

const myDog = new Dog();
myDog.breed
myDog.__proto__
// prototype sólo existe en las funciones
myDog.prototype
Dog.prototype

function Giraffe() {}
Giraffe.prototype

const koala = {};
// prototype es una propiedad que contiene un objeto
koala.prototype
koala.__proto__
// __proto__ es una referencia, no un objeto
koala.__proto__ === Object.prototype
```

### Ejercicio

Ejecutar el siguiente código en la consola y analizar qué pasa y por qué

```
// caso 1
const arr = [];
arr.__proto__ = null;

arr.push(1);
```

```
// caso 2
const arr = [];
arr.__proto__.push = function() {
  console.log('Nope 😈');
}

arr.push(1);
arr.push('a');
```

```
// caso 3
const arr = [];
arr.__proto__ = {}

arr.push(1);
```

```
// caso 4
const arr = [];
delete arr.__proto__.push;

arr.push(1);
```

- [delete operator - MDN](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Operators/delete)

## Las funciones son funciones... y objetos

- Recordemos que las funciones son _First-Class citizens_
- Por lo tanto podemos tratarlas como cualquier otro valor, por ejemplo pasarlas por parámetro o retornarlas desde otra función
- Por eso también decimos que las funciones en javascript son _funciones de alto orden_
- Y todo esto lo podemos hacer porque las funciones... son objetos!

```js
// creando funciones con la función constructora
const sum = new Function('a', 'b', 'return a + b');

console.log(sum(2, 6));
```

- [Function - MDN](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Function)

### Combo función-objeto

- Todas las funciones en JavaScript tienen por default una propiedad llamada `prototype` en su 'versión objeto'
  - Esta propiedad contiene incialmente un objeto "vacío", sin propiedades propias
- El valor de `prototype` es un objeto
  - Podemos agregarle propiedades y métodos, es decir _extenderlo_; incluso reemplazarlo por otro objeto que decidamos
- Este objeto es el que vamos a utilizar como prototipo, en el caso de que utilicemos esta función para construir nuevos objetos (estas funciones se conocen como _Factory Functions_)
- Por lo tanto, los nuevos objetos que creemos utilizando esta función, tendrán como prototipo al definido en la propiedad `prototype` de la función
  - Esto se logra seteando en el nuevo objeto una propiedad oculta, `__proto__` que es una **referencia** (no una copia!) a esta propiedad `prototype`, es decir, a su prototipo

```js
function multiplyBy2(num) {
  return num * 2;
}

multiplyBy2.stored = 5;
multiplyBy2(3); // 6

multiplyBy2.stored; // 5
multiplyBy2.prototype; // {}
```

## _Factory Function_ vs `constructor`

### _Factory Function_

- En JavaScript, cualquier función puede retornar un objeto. **Cuando no se trata de una función constructora o _clase_, la llamamos _Factory Function_**

```js
function Person(firstName, lastName, age) {
  const person = Object.create();

  // usamos `person`en lugar de `this` porque en este caso `this` no refiere al objeto nuevo que creamos, sino al global
  person.firstName = firstName;
  person.lastName = lastName;
  person.age = age;

  return person;
}

const person = Person('Dare', 'Devil', 32);
```

### `constructor`

- Por convención, se utiliza siempre la primer letra del nombre de la función en mayúscula para indicar que es una función constructora
- Se invocan utilizando la keyword `new`
- No necesitamos crear ni devolver el nuevo objeto a mano, `new` ya se encarga de eso
- :warning: No podemos utilizar _arrow functions_ como funciones constructoras ya que el `this` que utilizan no puede hacer referencia a un nuevo objeto creado

```js
function Person(firstName, lastName, age) {
  this.firstName = firstName;
  this.lastName = lastName;
  this.age = age;
}

const person = new Person('Dare', 'Devil', 32);
```

## `isPrototypeOf`, `getPrototypeOf` e `instanceof`

```js
function Professor(name, teaching, subjects) {
  this.name = name;
  this.isTeaching = teaching;
  this.subjects = subjects;
}

Professor.prototype = {
  showSubjects() {
    console.log(this.subjects);
  }
}

const professorX = new Professor('Charles Xavier', true, ['telepathy', 'leadership']);

console.log(Professor.prototype.isPrototypeOf(professorX));
console.log(Object.getPrototypeOf(professorX));
console.log(professorX instanceof Professor);
```

- `isPrototypeOf`: sirve para chequear si un objeto es prototipo de otro ó es la _clase_ que se usó para crearlo
- `getPrototypeOf`: retorna el prototipo (objeto) de un objeto
- `instanceof`: sirve para chequear si un objeto fue creado a partir de una determinada _función constructora_ o _clase_; un _objeto_ creado por un _constructor_ es una _instancia_ de ese _constructor_

## Creación de objetos

### `Object.create`

- Es un método de `Object` que crea un nuevo objeto, con el prototipo seteado a un cierto objeto
- Es más _natural_ para el modelo de prototipos que la keyword `new`
- **Utilizar `Object.create`en lugar de `Object.setPrototypeOf`**

```js
const animal = {
  init(sound) {
    this._sound = sound;
    return this;
  },
  talk() {
    console.log(this._sound);
  }
}

const cat = Object
  .create(animal)
  .init('meow!');

cat.talk();
```

### `new` keyword

1. Crea un nuevo objeto vacío, el cual asigna a `this`
2. Llama a la función _constructora_ ó _Factory Function_
  - Si llamamos a la función que construye el nuevo objeto (_Factory Function_) sin `new` adelante (podemos, porque es una función), `this` será una referencia al objeto global `window` y no funcionará como esperamos. Por eso a modo de indicación, se suele escribir la primer letra de estas funciones con mayúscula, para indicar que se debe invocar usando `new`
3. A este nuevo objeto le setea una propiedad oculta, `__proto__`, la cual tendrá una **referencia** a la propiedad`prototipe` (objeto) de la función
4. Si la _Factory Function_ recibe algún parámetro, los usa para setear propiedades de este nuevo objeto
5. Retorna el nuevo objeto

#### `new` behind the scenes

```js
function UserCreator(name, score) {
  // creamos un objeto vacío y lo enlazamos con su prototipo seteando su popiedad oculta __proto__
  const newUser = Object.create(userFunctions);
  // seteamos sus propiedades
  newUser.name = name;
  newUser.score = score;
  
  return newUser;
}

// `prototype`: el objeto nuevo va a heredar estas propiedades
const userFunctions = {
  increment() {
    this.score++;
  },
  login() {
    console.log('You have logged in');
  }
}

// creamos un nuevo usuario
const user = UserCreator('Sarah Connor', 7);
// interactuamos con el usuario a través de sus métodos
user.login();
```

- `new` automatiza todo este proceso

### `new` vs `Object.create`

- `Object.create` crea un nuevo objeto vacío y además le asigna a este el prototipo que nosotros querramos, si le pasamos un argumento, sino le asigna `Object` como prototipo
- `new` en cambio, es una llamada a una función constructora (ó _Factory Function_), la cual también puede recibir argumentos, pero en este caso son para setear otras propiedades del objeto y no su prototipo
  - En este caso, el prototipo del nuevo objeto se obtiene a partir de la propiedad `prototipe` (objeto) de la función, a la cual se setea una referencia en la propiedad `__proto__` del nuevo objeto
- Por último, con `Object.create` podemos crear un objeto que no herede de nadie (no tenga prototipo), usando `Object.create(null)`; mientras que, si seteamos `SomeConstructor.prototype = null`, el nuevo objeto va a heredar de `Object.prototype`

```js
const x = {
  prop1: ...,
  prop2: ...,
  ...
};

const object = Object.create() // prototipo de object : Object
const anotherObject = Object.create(x) // prototipo de anotherObject: x
const newObject = new SomeConstructor(); // => prototipo de newObject: SomeConstructor.prototype
```

## `bind`

```js
const kittie = {
  _sound: 'MEOW',
  talk() {
    console.log(this._sound);
  }
}

kittie.talk();

const talkFn = kittie.talk;
talkFn();
```

```js
const kittie = {
  _sound: 'MEOW',
  talk() {
    console.log(this._sound);
  }
}

kittie.talk();

const talkFn = kittie.talk.bind(kittie);
talkFn();
```

> :star: En una función, `this` hace referencia al contexto en el que fue llamada. Si es sólo una función y no un método, entonces su contexto será el objeto global (`window` en el browser, `global` en Node)

```js
function showMeThis() {
  console.log(this);
}
```

- Para forzar el contexto de una función, podemos utilizar `bind`

```js
function showMeThis() {
  console.log(this);
}

const user = {
  name: 'Ash Ketchum',
  email: 'ash@pokemonmaster.com'
}

const showMeThisUser = showMeThis.bind(user);
showMeThisUser();
```

```js
function showMeThis() {
  console.log(`name: ${this.name}, email: ${this.email}`);
}

const user = {
  name: 'Ash Ketchum',
  email: 'ash@pokemonmaster.com',
  info: showMeThis
}

user.info();
```

- `bind` es un método de `Function`, que retorna una nueva función (setea el `this`), con un nuevo contexto... Se acuerdan que en JS las funciones eran funciones y objetos a la vez?

> :star: El valor de `this` depende del contexto en el cual se llama a una función. Este contexto está dado por un objeto.

- Usando `bind` hacemos explícito el contexto
- Más info: [`bind` - MDN](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_objects/Function/bind)

## El problema que tenemos al usar `this`

- Las funciones pueden tener 2 tipos de parámetros: _explícitos_ (los que definimos nosotros) e _implícitos_. Estos últimos son parámetros que las funcionen tienen y nosotros no definimos

```js
// en esta función, a y b son parámetros explícitos
function sum(a, b) {
  return a + b;
}
```

- **`this` es un _parámetro implícito_ que tienen todas las funciones en JS. Hace referencia al contexto actual y por contexto queremos decir _un objeto_**
- **Por default, `this` no hace referencia al contexto en el que se creó la función, sino al contexto en que fue invocada** (_salvo que usemos arrow functions_) **es decir, desde dónde la estamos llamando**
- Cuando la función es un método de un objeto, `this` hace referencia al objeto a la izquierda del `.`
  - Este es el comportamiento default de `this` en la mayoría de los lenguajes orientados a objetos

```js
const ball = {
  position: {
    x: 20,
    y: 40
  },
  color: 'red',
  size: 2,
  describe() {
    console.log(this);
  }
};
```

- Si es una función cualquiera, `this` hace referencia al contexto global (objeto `window` en el browser y `global` en Node)
- :warning: **Recuerden que siempre que entramos a una función, estamos generando un _nuevo contexto de ejecución_, por eso cambia**

```
// `this` es una referencia al objeto `context`
context.method();
```

```js
// contexto global
function playVideo() {
  console.log(this);
}

playVideo();
```

```js
function Video(title) {
  this._title = title;
  console.log(this);
}

const video = new Video('V/H/S');
```

- :question: Qué pasa si tenemos funciones dentro de algún método, para modularizar el código?
  - Quién sería `this`en este caso, si no estamos invocando un método? :question:

```js
function User(name, score) {
  this._name = name;
  this._score = score;
}

// a qué hace referencia `this` en este caso?
User.prototype.increment = function() {
  function addOne() {
    this._score++;
  }

  addOne();
} 

User.prototype.login = function() {
  console.log('login');
}

const user = new User("Eva", 23);
user.increment();
```

- :warning: **Recuerden que todas las funciones tienen su `this` y que si no le aclaramos cuál es, va a usar el global (`window`, `global`)**
- Este es otro de los conceptos que más confusión generan en JS
- Gran fuente de bugs
- Algo que muy probablemente les pregunten en una entrevista para hacerles caer en la trampa si hablan de objetos en JS

### Cómo forzar el valor de `this`

#### Solución 1

- Guardamos el contexto antes, para desp hacer referencia

```js
function User(name, score) {
  this._name = name;
  this._score = score;
}

User.prototype.increment = function() {
  // guardamos el contexto antes de definir la nueva función
  const self = this;
  
  // ahora `self`es una referencia al `this` anterior
  function addOne() {
    self._score++;
  }

  addOne();
} 

User.prototype.login = function() {
  console.log('login');
}

const user = new User("Eva", 23);
user.increment();
```

#### Solución 2 (mejor que la 1)

- Forzamos el contexto, usando `bind`

```js
function User(name, score) {
  this._name = name;
  this._score = score;
}

User.prototype.increment = function() {
  const bindedAddOne = (function addOne() {
    this._score++;
  }).bind(this);

  bindedAddOne();
} 

User.prototype.login = function() {
  console.log('login');
}

const user = new User("Eva", 23);
user.increment();
```

#### Solución 3 (la mejor de las 3)

- Feat. _ES6 arrow functions_! 🙌:fireworks:

```js
function User(name, score) {
  this._name = name;
  this._score = score;
}

User.prototype.increment = function() {
  // el `this` de la función `addOne` va a hacer referencia al valor de `this`en el momento de ser declarada (igual que `self` en la primer solución)
  const addOne = () => this._score++;

  addOne();
} 

User.prototype.login = function() {
  console.log('login');
}

const user = new User("Eva", 23);
user.increment();
```

![](https://res.cloudinary.com/practicaldev/image/fetch/s--nHNR2C2C--/c_limit%2Cf_auto%2Cfl_progressive%2Cq_auto%2Cw_880/https://thepracticaldev.s3.amazonaws.com/i/ec9exwlnw21ynkusaoks.png)

- Cuando usamos _arrow functions_, `this` es asignado automáticamente al contexto (el `this`) dentro del cual la función fue declarada
  - Esto es lo que se conoce como _lexical scoping_
- Además de [bind](https://github.com/undefinedschool/oop-js/blob/master/README.md#bind), podemos utilizar otros métodos similares como [`call`](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Function/call) y [`apply`](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Function/apply) para _tomar el control_ y setear manualmente el valor que se le asigna a `this`

### :warning: Ojo con `this`, los métodos y las _arrow functions_!

```js
const obj = {
  normalFn() {
    console.log(this);
  },
  arrowFn: () => console.log(this)
}

obj.normalFn();
obj.arrowFn();
```

- `normalFn` es una _función común_ que invocamos como _método de un objeto_, por eso el valor de `this` pasa a ser el objeto, pero `arrowFn` es una _arrow function_ y el valor de `this` al momento de definirla era `global`
- Por eso es recomendable usar _arrow functions_ para los _callbacks_ y funciones comunes para definir métodos
- [Tampoco podemos forzar el valor de `this`](https://www.youtube.com/watch?v=mBwwfts6af4) en una _arrow function_

### Bonus: algunos métodos tienen un `this` como parámetro opcional...

- Se acuerdan, por ejemplo del parámetro opcional [`thisArg`](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array/forEach#Parameters) del `forEach`?
- Ahora nos viene bien! :rocket:

```js
const video = {
  title: 'V/H/S',
  tags: ['horror', 'indie', 'thriller'],
  showTags() {
    this.tags.forEach(function(tag) {
      console.log(this.title, tag);
    })
  }
}

video.showTags();
```

#### Miremos el valor de `this`... 🤔

```js
const video = {
  title: 'V/H/S',
  tags: ['horror', 'indie', 'thriller'],
  showTags() {
    this.tags.forEach(function(tag) {
      console.log(this, tag);
    })
  }
}

video.showTags();
```

#### Qué pasa si usamos _arrow functions_? 🤔

```js
const video = {
  title: 'V/H/S',
  tags: ['horror', 'indie', 'thriller'],
  showTags() {
    this.tags.forEach(tag => console.log(this.title, tag))
  }
}

video.showTags();
```

#### Usando el parámetro opcional `thisArg`

```js
const video = {
  title: 'V/H/S',
  tags: ['horror', 'indie', 'thriller'],
  showTags() {
    this.tags.forEach(function(tag) {
      console.log(this.title, tags);
    }, this)
  }
}

video.showTags();
```

### tl;dr: Cómo saber el valor de `this`

#### `this` es...

1. un _parámetro implícito_ que tienen todas las funciones en JS
2. un **objeto que representa el contexto actual de ejecución** (en el cuál estamos ejecutando una función)

#### El valor de `this` depende de varios factores...

1. si es una función común y corriente, `this` hace referencia al _contexto global_ (`Window` en el browser, `global` en Node)
2. si es un método `m` de un objeto `x` y lo invocamos como `x.m()`, `this` hace referencia al objeto `x`
3. si utilizamos una función constructora, que invocamos usando la keyword `new`, `this` hace referencia al nuevo objeto que creamos
4. si usamos _arrow functions_, el valor de `this` está definido por lo que llamamos _lexical scope_, es decir, `this` **mantiene el valor que tenía en el lugar donde definimos la función, no se crea un _nuevo contexto_**
5. hay métodos que tienen un [parámetro opcional](https://github.com/undefinedschool/oop-js/blob/master/README.md#bonus-algunos-m%C3%A9todos-tienen-un-this-como-par%C3%A1metro-opcional) para setear el valor de `this`, por ejemplo algunos de _Array_
6. en el caso de ser necesario, podemos forzar el valor de `this` de [diversas formas](https://github.com/undefinedschool/oop-js/blob/master/README.md#c%C3%B3mo-forzar-el-valor-de-this)

#### :star: _Modos_

- Como truco, podemos hacer una analogía con los modos de las cámaras de fotos: `this` tiene 3 modos, _`auto`_, _`semi`_ y _`manual`_. 
  - _`auto`_: el valor de `this` se setea automáticamente según el contexto (ver ítems [_1, 2 y 3_](https://github.com/undefinedschool/oop-js/blob/master/README.md#el-valor-de-this-depende-de-varios-factores))
  - _`semi`_: tenemos algo de control sobre el valor de `this`, aunque se define de forma _implícita_, utilizando _arrow functions_ (ver ítem [_4_](https://github.com/undefinedschool/oop-js/blob/master/README.md#el-valor-de-this-depende-de-varios-factores))
  - _`manual`_: tenemos todo el control y nosotros definimos _explícitamente_ el valor de `this` (ver ítems [_5 y 6_](https://github.com/undefinedschool/oop-js/blob/master/README.md#el-valor-de-this-depende-de-varios-factores))

## Class

### `Prototype` version vs `Class` version

```js
function User(email, name) {
  this._email = email;
  this._name = name;
}

User.prototype.login = function() {
  console.log(`${this._email} just logged in`);
};

User.prototype.getEmail = function() {
  return this._email;
};

User.prototype.getName = function() {
  return this._name;
};

const userOne = new User('ryu@ninjas.com', 'Ryu');
userOne.login();

// check logs
console.log(userOne.__proto__);
console.log(User.prototype);
console.dir(userOne);
console.dir(userOne.__proto__);
console.dir(User.prototype);
console.log(userOne.__proto__ === User.prototype);
```

- Al definir los métodos dentro de una clase, JS se encarga por nosotros de definirlos en el `prototype` de la función constructora (ó _Factory Function_)
- Renombramos la _parte función_ del combo _función-objeto_ `User` como `constructor`
- **`Class User` es nuestra vieja y conocida función constructora, con otra sintaxis!**

```js
// aplicando un poco de syntax sugar...
class User {
  constructor(email, name) {
    this._email = email;
    this._name = name;
  }

  login() {
    console.log(`${this._email} just logged in`);
  }

  getEmail() {
    return this._email;
  }

  getName() {
    return this._name;
  }
}

const userOne = new User('ryu@ninjas.com', 'Ryu');
userOne.login();

// check logs
console.log(userOne.__proto__);
console.log(User.prototype);
console.dir(userOne);
console.dir(userOne.__proto__);
console.dir(User.prototype);
console.log(userOne.__proto__ === User.prototype);
```

### Herencia con `Class`

```js
class Mammal {
  constructor(sound) {
    this._sound = sound;
  }

  talk() {
    return this._sound;
  }
}

const fluffy = new Mammal('woof');
fluffy.talk();
```

```js
class Mammal {
  constructor(sound) {
    this._sound = sound;
  }

  talk() {
    return this._sound;
  }
}

// herencia
class Dog extends Mammal {
  constructor() {
    super('woOoOof!');
  }
}

const fluffy = new Dog();
fluffy.talk();

// BOOM!
console.log(typeof Dog);
console.log(Dog.prototype.isPrototypeOf(fluffy));
```

- [`super`](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Operators/super) es una _keyword_ que utilizamos para acceder a propiedades y métodos de una _superclase_, por ejemplo el constructor
- :warning: JavaScript no tiene clases! Es sólo _sugar syntax_ sobre lo que ya conocemos de prototipos
- :question: **En los ejemplos que vimos recién, cuáles serían los prototipos?**
- :star: Si usamos `Class`, la `new` keyword es requerida para crear nuevos objetos (no pasa si usamos las funciones de siempre y tiene consecuencias sobre el `this`)

### Herencia basada en prototipos (Prototypal Inheritance)

#### 1. Constructor

- Los _constructores_ nos permiten construir e inicializar objetos
- **Son funciones**, que pueden tomar ciertos argumentos y setearlos como propiedades del nuevo objeto
- Por convención y para distinguirlos de otras funciones, se suele escribir _la primer letra en mayúscula_
- Los invocamos utilizando la keyword `new`

```js
function PokeBall(size, color) {
   // props
   this._size = size;
   this._color = color;

   // methods
   this.getSize = function() {
     console.log(this._size);
   };
   this.getColor = function() {
     console.log(this._color);
   }
};

const ultraBall = new PokeBall(3, 'black');
```

#### 2. Seteando el prototipo

- Los objetos creados sin un prototipo seteado explícitamente, tendran como prototipo al objeto `Object`
- El prototipo se setea en la propiedad `prototype` de la función constructora

##### Forma 1: adjuntando métodos 

```js
function PokeBall(size, color) {
   this._size = size;
   this._color = color;
};

PokeBall.prototype.getSize = function() {
  console.log(this._size);
}

PokeBall.prototype.getColor = function() {
  console.log(this._color);
}

const ultraBall = new PokeBall(3, 'black');

// ver las propiedades de la función/objeto constructora
console.dir(PokeBall);
```

##### Forma 2: definiendo un objeto como prototipo

```js
const protoPokeBall = {
  getSize() {
    console.log(this._size);
  },
  getColor() {
    console.log(this._color);
  }
};

function PokeBall(size, color) {
   this._size = size;
   this._color = color;
};

PokeBall.prototype = protoPokeBall;

const ultraBall = new PokeBall(3, 'black');

// ver las propiedades de la función/objeto constructora
console.dir(PokeBall);
```

#### Otro ejemplo de herencia basada en prototipos (`extends` & _subclass_ behind the scenes)

```js
function UserCreator(name, score) {
  // creamos un objeto vacío y lo enlazamos con su prototipo seteando su popiedad oculta __proto__
  const newUser = Object.create(userFunctions);
  // seteamos sus propiedades
  newUser.name = name;
  newUser.score = score;
  
  return newUser;
}

// `prototype`: el objeto nuevo va a heredar estas propiedades
const userFunctions = {
  increment() {
    this.score++;
  },
  login() {
    console.log(`${this.name} has logged in`);
  }
}

function paidUserCreator(paidName, paidScore, accountBalance) {
  const newPaidUser = UserCreator(paidName, paidScore);
  Object.setPrototypeOf(newPaidUser, paidUserFunctions);
  newPaidUser.accountBalance = accountBalance;

  return newPaidUser;
}

const paidUserFunctions = {
  increaseBalance() {
    this.accountBalance++;
  }
};

// creamos un nuevo usuario normal
const user = UserCreator('Sarah Connor', 7);
// interactuamos con el objeto a través de sus métodos
user.login();
// establecemos la cadena de prototipos
Object.setPrototypeOf(paidUserFunctions, userFunctions);
// creamos un nuevo usuario pago
const paidUser = paidUserCreator('Alyssa', 8, 25);
// invocamos métodos del nuevo objeto pago
paidUser.login()
paidUser.increaseBalance();

console.dir(user);
console.dir(paidUser);
console.dir(user.__proto__);
console.dir(paidUser.__proto__);
```

- Usamos la ya conocida _Prototype Chain_
- Si usamos `Class`, para que una 'clase' (falsa) herede de otra, es decir, sea una _subclase_, usamos `extends`
  - De esta forma, los objetos creados a partir de la 'subclase' (falsa) heredarán propiedades definidas en esta y en la 'superclase'

```js
class Dog extends Mammal {
  constructor() {
    // llamamos al constructor de la superclase
    super('woOoOof!');
  }
}
```

- Un objeto puede sobreescribir un método de su prototipo y tiene precedencia sobre este otro

```js
const protoObj = {
  logX() {
    console.log('x');
  }
}

const obj = Object.create(protoObj);
obj.logX = function() {
  console.log('<xXx>');
};
obj.logX(); // '<xXx>'
```

```js
class User {
  constructor(email, name) {
    this._email = email;
    this._name = name;
    this._score = 0; 
  }

  login() {
    console.log(`${this._email} just logged in`);
  }

  logout() {
    console.log(`${this._email} just logged out`);
  }
  
  updateScore() {
    this._score++;
    console.log(`${this._user}'s score is now ${this._score}`);
  }
}

class Admin extends User {
  deleteUser(ripUser) {
    users = users.filter(user => user.email !== ripUser.email);
  }
}

const ryu = new User('ryu@sf2.com', 'Ryu');
const ken = new User('ken@sf2.com', 'Ken');
const admin = new Admin('chunli@sf2.com', 'Chun-Li');
const users = [ryu, ken, admin];

console.log(users);
admin.deleteUser(ken);
console.log(users);
```

### `Class` behind the scenes

```js
function User(email, name) {
  this._email = email;
  this._name = name;
}

User.prototype.login = function() {
  console.log(`${this._email} just logged in`);
}
  
User.prototype.logout = function() {
  console.log(`${this._email} just logged out`);
}

const ryu = new User('ryu@sf2.com', 'Ryu');
const ken = new User('ken@sf2.com', 'Ken');
console.log(ken);
ryu.login();
```

## Polimorfismo

- La palabra viene del griego _poli_ (muchos) y _morfo_ (forma), muchas formas
- **Definición formal:** propiedad que nos **permite enviar mensajes sintácticamente iguales (es decir, que se llaman igual y toman los mismos parámetros) a objetos de tipos distintos**. El único requisito que deben cumplir los objetos que se utilizan de manera polimórfica es saber responder al mensaje que se les envía
- _tl;dr_ Propiedad que permite que objetos de diferentes tipos/'clases' puedan responder a los mismos mensajes/métodos
  - Esto se logra sobreescribiendo un método de una clase en una subclase
- Propiedad que nos permite tratar de la misma forma a objetos de tipos diferentes
- Cuando hablamos de _objetos de diferentes tipos_ en el contexto de _polimorfismo_, nos referimos a objetos cuyos prototipos son diferentes ó que son (con muchas comillas) _'instancias'_ de diferentes _'clases'_

### Usando prototipos

#### Estableciendo la herencia

```js
const User = {
  active: false,
  sayHello() {
    console.log(`${this.name} says hi!`)
  }
};

const Student = {
  name: 'Morty',
  major: 'JavaScript'
};

const Professor = {
  name: 'Rick',
  teaching: ['JavaScript', 'NodeJS', 'Physics']
};

Object.setPrototypeOf(Student, User);
Object.setPrototypeOf(Professor, User);

Student.active = true;

const newUsers = [Student, Professor];

newUsers.forEach(user => user.sayHello())
```

#### Sobreescribiendo métodos del prototipo

```js
const User = {
  active: false,
  describe() {
    console.log(`${this.name} says hi!`)
  }
};

const Student = {
  name: 'Morty',
  major: 'JavaScript',
  describe() {
    console.log(`${this.name} studies ${this.major}`);
  }
};

const Professor = {
  name: 'Rick',
  teaching: ['JavaScript', 'NodeJS', 'Physics'],
  describe() {
    console.log(`${this.name} teaches ${this.teaching}`);
  }
};

Object.setPrototypeOf(Student, User);
Object.setPrototypeOf(Professor, User);

Student.active = true;

const newUsers = [Student, Professor];

newUsers.forEach(user => user.describe())
```

### Usando  `Class`

```js
class Animal {
  constructor(name) {
    this._name = name;
  }

  makeSound() {
    console.log('🔉 Default sound!');
  }
}

class Dog extends Animal {
  constructor(name) {
    super(name);
  }

  makeSound() {
    console.log('🐶 WoOof!')
  }
}

class Cat extends Animal {
  constructor(name) {
    super(name);
  }

  makeSound() {
    console.log('🐱 MeowW!')
  }
}

const animal = new Animal('Doggie');
animal.makeSound();

const dog = new Dog('Beethoven');
const cat = new Cat('Felix');
dog.makeSound();
cat.makeSound();
```

## _Getters_ & _Setters_

```js
const person = {
  firstName: 'Aquiles',
  lastName: 'Bailoyo',
  // the old way...
  getFullName() {
    return `${this.firstName} ${this.lastName}`
  }
};

console.log(person.getFullName());
```

- *Contras de usar este approach:*
  1. una vez creado el objeto, sus propiedades `firstName`y `lastName` son _read-only_ (sólo lectura), no podemos modificar el valor
  2. tenemos que utilizar un _método_ para algo que tal vez estaría bueno tener como el valor de una _propiedad_ común

### Usando `get`

```js
const person = {
  firstName: 'Aquiles',
  lastName: 'Bailoyo',
  get fullName() {
    return `${this.firstName} ${this.lastName}`
  }
};

console.log(person.fullName);
```

### Usando `get` y `set`

```js
const person = {
  firstName: 'Aquiles',
  lastName: 'Bailoyo',
  get fullName() {
    return `${this.firstName} ${this.lastName}`
  },
  set fullName(name) {
    const fullName = name.split(' ');
    this.firstName = fullName[0];
    this.lastName = fullName[1];
    console.info(`${name} has been set as person's full name.`)
  }
};

// usando el _setter_
person.fullName = 'Armando Paredes';
// usando el _getter_
console.log(person.fullName);
```

### tl;dr

- Los _getters_ y _setters_ son _métodos_ definidos en un objeto o clase, que se ven y utilizamos "como si fueran propiedades"
- Forman parte de la _interfaz_ del objeto, es decir, son públicos
- Son _features_ de _ES6/2015+_
- La idea es que accedamos y modifiquemos propiedades del objeto _de forma segura y controlada_, a través de los _getters_ y _setters_
- Usamos _getters_ para _acceder/obtener_ al valor de una propiedad
- Usamos _setters_ para _setear/modificar/mutar_ el valor de una propiedad

## Métodos _estáticos_

- Son métodos que se definen dentro de una _clase_ y podemos utilizar sin necesidad de _instanciarla_ (crear un objeto a partir de esta clase)
- No son métodos que accedemos y utilizamos directamente desde una _instancia_ (objeto)
- Se definen directamente en el constructor (_función constructora_ ó _clase_), con la keyword `static` delante
- Se invocan con la sintaxis `Clase.método()`
- Se suelen utilizar como _métodos utilitarios_ para funcionalidad y operaciones que no tienen que ver directamente con el comportamiento de los objetos

```js
class Square {
  constructor(width) {
    this._width = width;
    this._height = width;
  }

  get area() {
    return this._width ** 2;
  }

  set area(newArea) {
    this._width = Math.sqrt(newArea);
    this._height = Math.sqrt(newArea);
  }
  
  static isEqual(aSquare, anotherSquare) {
    return aSquare.area === anotherSquare.area;
  }
}

const squareA = new Square(5);
const squareB = new Square(7);

console.log(Square.isEqual(squareA, squareB));

const squareC = new Square(5);
console.log(Square.isEqual(squareA, squareC));
```

## POO: Conceptos fundamentales explicados brevemente

- **Objeto:** colección de datos/funcionalidades relacionados (variables y funciones), que llamamos _propiedades_
- **Propiedad:** par _clave-valor_ que almacenamos en un objeto, donde el valor puede ser algún tipo primitivo de JS u otro objeto
- **Método:** propiedad de un objeto cuyo valor es una función. Función ligada a un objeto
- **Encapsulación:** Separación entre la _interfaz_ del objeto y su implementación. Interactuamos con los objetos sólo a través de las propiedades y métodos que nos exponen en su _interfaz_ y no de otra forma
- **Herencia:** un objeto puede acceder y utilizar propiedades/métodos definidos en su prototipo, o en el prototipo de su prototipo, etc, lo que llamamos su _Prototype Chain_. Básicamente es una transferencia de propiedades entre objetos, de _'arriba' hacia 'abajo'_ en la cadena. **Es el mecanismo para reutilizar código que nos brinda el paradigma.**
- **Polimorfismo:** propiedad que permite que objetos de diferentes tipos o 'clases' puedan responder a los mismos mensajes/métodos. Esto se logra sobreescribiendo un método de una clase en una subclase y nos permite _tratar de la misma forma a objetos de tipos diferentes_

## :fireworks: Bonus

### :question: Cómo hacemos para iterar sobre las propiedades de un objeto?

#### 1. Iterar sobre _todas_ las propiedades del objeto, incluyendo las que hereda de su _prototipo_

```js
for (const key in obj) {
  console.log(`key: ${key}, value: ${obj[key]}`);
}
```

#### 2. Iterar sólo sobre las propiedades _propias_ (las que definimos explícitamente) del objeto

```js
for (const key in obj) {
  if (obj.hasOwnProperty(key)) {
    console.log(`key: ${key}, value: ${obj[key]}`);
  }
}
```

### :question: Cómo hacemos para clonar un objeto?

### Solución 1

```js
// iterando las keys del objeto original y agregándolas con sus valores a la copia
const circle = {
  radius: 1,
  draw() {
    console.log('draw');
  }
}

const circleClone = {};

for (key in circle) {
  circleClone[key] = circle[key];
}
```

### Solución 2

```js
const circle = {
  radius: 1,
  draw() {
    console.log('draw');
  }
}

const circleClone = Object.assign({}, circle);

// con `Object.assign()` también podemos sobreescribir algunas propiedades si le pasamos otro parámetro
const circleWithBiggerRadius = Object.assign({}, circle, { radius: 3 });
```

### Solución 3

```js
// the ninja way
const circle = {
  radius: 1,
  draw() {
    console.log('draw');
  }
}

const circleClone = {...circle};
```

:warning: **Nota:** estas formas sólo sirven para hacer _shallow cloning_ (ó _shallow copy_), es decir, copias de 1 sólo nivel de profundidad, sin tener en cuenta objetos anidados. Sirve para objetos simples. Si queremos hacer una copia completa, debemos hacer una función que copie recursivamente ó usar [algún método de alguna lib como _Lodash_](https://lodash.com/docs/4.17.15#cloneDeep)

De [**MDN**](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Operators/Spread_syntax#Spread_in_array_literals):

![](https://i.imgur.com/9XAXrBc.png)

## Para seguir aprendiendo...

- [Working with Objects - MDN](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Guide/Working_with_Objects)
- [Inheritance and the prototype chain - MDN](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Inheritance_and_the_prototype_chain)
- [Details_of_the_Object_Model - MDN](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Guide/Details_of_the_Object_Model)

## 📚 Libros recomendados sobre OOP en JS

- [The Principles Of Object-oriented Javascript](https://www.bookdepository.com/Principles-Object-oriented-Javascript-Nicholas-C-Zakas/9781593275402/?a_aid=nhsz)
- [Learning JavaScript Design Patterns](https://www.bookdepository.com/Learning-JavaScript-Design-Patterns-Addy-Osmani/9781449331818/?a_aid=nhsz)
- [Design Patterns : Elements of Reusable Object-Oriented Software](https://www.bookdepository.com/Design-Patterns-Erich-Gamma/9780201633610/?a_aid=nhsz)

## :star: Conclusión

> La idea de usar paradigmas (como POO) es tener herramientas para organizar mejor nuestro código, para que sea más legible, fácil de razonar, mantenible, etc. 

> _Programación Orientada a Objetos_ es un _paradigma de programación_ que utiliza _objetos_ para modelar _entidades_ del mundo real

> En el caso de POO, lo que nos interesa principalmente es encapsular/empaquetar datos relacionados con funciones que podemos aplicar sobre esos datos y dividir nuestro programa en estos objetos, que interactúan entre si a traves de su interfaz, intercambiando mensajes
