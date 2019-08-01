# Notas sobre Programación Orientada a Objetos en JS

> El siguiente contenido fue elaborado por [@_nhsz](https://twitter.com/_nhsz) como guía para las clases relacionadas a OOP de [undefined school](https://undefinedschool.io)

> Son bienvenidos los _issues_ y _PRs_ para mejorar el contenido, corregir errores, etc

> Si el contenido te resultó útil y querés colaborar, podés hacerlo [acá](https://trello.com/c/TFbCZtPN/34-donaciones) (se acepta BTC :P). Gracias!

## Índice

- [Objetos](https://github.com/undefinedschool/oop-js/blob/master/README.md#objetos)
  - [Sintaxis](https://github.com/undefinedschool/oop-js/blob/master/README.md#sintaxis)
- [POO](https://github.com/undefinedschool/oop-js/blob/master/README.md#poo)
- [Prototype](https://github.com/undefinedschool/oop-js/blob/master/README.md#prototype)
  - [Herencia basada en prototipos (_Prototypal Inheritance_)](https://github.com/undefinedschool/oop-js/blob/master/README.md#herencia-basada-en-prototipos-prototypal-inheritance)
- [Las funciones son funciones... y objetos
](https://github.com/undefinedschool/oop-js/blob/master/README.md#las-funciones-son-funciones-y-objetos)
  - [Combo función-objeto](https://github.com/undefinedschool/oop-js/blob/master/README.md#combo-funci%C3%B3n-objeto)
- [`Object.create`](https://github.com/undefinedschool/oop-js/blob/master/README.md#objectcreate)
- [`new` keyword](https://github.com/undefinedschool/oop-js/blob/master/README.md#new-keyword)
  - [`new` behind the scenes](https://github.com/undefinedschool/oop-js/blob/master/README.md#new-behind-the-scenes)
- [`new` vs `Object.create`](https://github.com/undefinedschool/oop-js/blob/master/README.md#new-vs-objectcreate)
- [`bind`](https://github.com/undefinedschool/oop-js/blob/master/README.md#bind)
- [El problema que tenemos al usar `this`](https://github.com/undefinedschool/oop-js/blob/master/README.md#el-problema-que-tenemos-al-usar-this)
- [`Class`](https://github.com/undefinedschool/oop-js/blob/master/README.md#class)
  - [Herencia con `Class`](https://github.com/undefinedschool/oop-js/blob/master/README.md#herencia-con-class)
  - [`Class` behind the scenes](https://github.com/undefinedschool/oop-js/blob/master/README.md#class-behind-the-scenes)
- [Polimorfismo](https://github.com/undefinedschool/oop-js/blob/master/README.md#polimorfismo)
  - [Usando prototipos](https://github.com/undefinedschool/oop-js/blob/master/README.md#usando-prototipos)
  - [Usando `Class`](https://github.com/undefinedschool/oop-js/blob/master/README.md#usando--class)
- [POO: Conceptos fundamentales explicados brevemente](https://github.com/undefinedschool/oop-js/blob/master/README.md#poo-conceptos-fundamentales-explicados-brevemente)
- [Bonus: Cómo hacemos para clonar un objeto?](https://github.com/undefinedschool/oop-js/blob/master/README.md#question-c%C3%B3mo-hacemos-para-clonar-un-objeto)
- [Para seguir leyendo...](https://github.com/undefinedschool/oop-js/blob/master/README.md#para-seguir-leyendo)
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

### Prototype

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
- Podemos _aumentar_ o _extender_ el prototipo de una función constructora ya existente modificando su propiedad `prototype` y todos los objetos creados con esta función tendrán las nuevas propiedades

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

#### Ejercicio

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

### Las funciones son funciones... y objetos

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

#### Combo función-objeto

- Todas las funciones en JavaScript tienen por default una propiedad llamada `prototype` en su 'versión objeto'
  - Esta propiedad contiene incialmente un objeto "vacío", sin propiedades propias
- El valor de `prototype` es un objeto
  - Podemos agregarle propiedades y métodos, es decir _extenderlo_; incluso reemplazarlo por otro objeto que decidamos
- Este objeto es el que vamos a utilizar como prototipo, en el caso de que utilicemos esta función como función constructora
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
2. Llama a la función constructora
  - Si llamamos a la función constructora sin `new` adelante (podemos, porque es una función), `this` será una referencia al objeto global `window` y no funcionará como esperamos. Por eso a modo de indicación, se suele escribir la primer letra de estas funciones con mayúscula, para indicar que se debe invocar usando `new`
3. A este nuevo objeto le setea una propiedad oculta, `__proto__`, la cual tendrá una **referencia** a la propiedad`prototipe` (objeto) de la función
4. Si la función constructora recibe algún parámetro, los usa para setear propiedades de este nuevo objeto
5. Retorna el nuevo objeto

#### `new` behind the scenes

```js
function UserCreator(name, score) {
  // creamos un objeto vacío y lo enlazamos con su prototipo seteando su popiedad oculta __proto__
  const newUser = Object.create(userFunctionStore);
  // seteamos sus propiedades
  newUser.name = name;
  newUser.score = score;
  
  return newUser;
}

// `prototype`. El objeto nuevo va a heredear estas propiedades
const userFunctionStore = {
  increment() {
    this.score++;
  }

  login() {
    console.log('You have logged in');
  }
}

// creamos nuevos objetos
const user1 = UserCreator('Sarah Connor', 7);
const user2 = UserCreator('John Connor', 4);
```

- `new` automatiza todo este proceso

### `new` vs `Object.create`

- `Object.create` crea un nuevo objeto vacío y además le asigna a este el prototipo que nosotros querramos, si le pasamos un argumento, sino le asigna `Object` como prototipo
- `new` en cambio, es una llamada a una función constructora, la cual también puede recibir argumentos, pero en este caso son para setear otras propiedades del objeto y no su prototipo
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

### `bind`

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

### El problema que tenemos al usar `this`

- `this` es un _parámetro implícito_ que tienen todas las funciones en JS. Hace referencia al contexto actual y por contexto queremos decir _un objeto_
  - Cuando la función es un método de un objeto, `this` hace referencia al objeto a la izquierda del `.`
  - Si es una función cualquiera, `this` hace referencia al contexto global (objeto `window` en el browser y `global` en Node)
    - :warning: Recuerden que siempre que entramos a una función, estamos generando un _nuevo contexto de ejecución_, por eso cambia

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

- Featuring... _ES6 arrow functions_! 🙌:fireworks:

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

- Cuando usamos _arrow functions_, `this` es asignado automáticamente al contexto (el `this`) dentro del cual la función fue declarada
  - Esto es lo que se conoce como _lexical scoping_

#### Bonus: algunos métodos tienen un `this` como parámetro opcional...

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

```js
// usando el parámetro opcional
const video = {
  title: 'V/H/S',
  tags: ['horror', 'indie', 'thriller'],
  showTags() {
    this.tags.forEach(function(tag) {
      console.log(this.title, tag);
    }, this)
  }
}

video.showTags();
```

### Class

#### `Prototype` version vs `Class` version

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

- Al definir los métodos dentro de una clase, JS se encarga por nosotros de definirlos en el `prototype` de la función constructora
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

#### Herencia con `Class`

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

### Polimorfismo

- La palabra viene del griego _poli_ (muchos) y _morfo_ (forma), muchas formas
- **Definición formal:** propiedad que nos **permite enviar mensajes sintácticamente iguales (es decir, que se llaman igual y toman los mismos parámetros) a objetos de tipos distintos**. El único requisito que deben cumplir los objetos que se utilizan de manera polimórfica es saber responder al mensaje que se les envía
- _tl;dr_ Propiedad que permite que objetos de diferentes tipos/'clases' puedan responder a los mismos mensajes/métodos
  - Esto se logra sobreescribiendo un método de una clase en una subclase
- Propiedad que nos permite tratar de la misma forma a objetos de tipos diferentes
- Cuando hablamos de _objetos de diferentes tipos_ en el contexto de _polimorfismo_, nos referimos a objetos cuyos prototipos son diferentes ó que son (con muchas comillas) _'instancias'_ de diferentes _'clases'_

#### Usando prototipos

##### Estableciendo la herencia

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

##### Sobreescribiendo métodos del prototipo

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

#### Usando  `Class`

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

## POO: Conceptos fundamentales explicados brevemente

- **Objeto:** colección de datos/funcionalidades relacionados (variables y funciones), que llamamos _propiedades_
- **Propiedad:** par clave-valor, donde el valor puede ser algún tipo primitivo de JS u otro objeto
- **Método:** propiedad de un objeto cuyo valor es una función. Función ligada a un objeto
- **Encapsulación:** Separación entre la _interfaz_ del objeto y su implementación. Interactuamos con los objetos sólo a través de las propiedades y métodos que nos exponen en su _interfaz_ y no de otra forma
- **Herencia:** un objeto puede acceder y utilizar propiedades/métodos definidos en su prototipo, o en el prototipo de su prototipo, etc, lo que llamamos su _Prototype Chain_. Básicamente es una transferencia de propiedades entre objetos, de _'arriba' hacia 'abajo'_ en la cadena. **Es el mecanismo para reutilizar código que nos brinda el paradigma.**
- **Polimorfismo:** propiedad que permite que objetos de diferentes tipos o 'clases' puedan responder a los mismos mensajes/métodos. Esto se logra sobreescribiendo un método de una clase en una subclase y nos permite _tratar de la misma forma a objetos de tipos diferentes_

### :question: **Bonus: Cómo hacemos para clonar un objeto?**

#### Solución 1

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

#### Solución 2

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

## Para seguir leyendo...

- [Working with Objects - MDN](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Guide/Working_with_Objects)
- [Inheritance and the prototype chain - MDN](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Inheritance_and_the_prototype_chain)
- [Details_of_the_Object_Model - MDN](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Guide/Details_of_the_Object_Model)

## :star: Conclusión

> La idea de usar paradigmas (como POO) es tener herramientas para organizar mejor nuestro código, para que sea más legible, fácil de razonar, mantenible, etc. 

> _Programación Orientada a Objetos_ es un _paradigma de programación_ que utiliza _objetos_ para modelar _entidades_ del mundo real

> En el caso de POO, lo que nos interesa principalmente es encapsular/empaquetar datos relacionados con funciones que podemos aplicar sobre esos datos y dividir nuestro programa en estos objetos, que interactúan entre si a traves de su interfaz, intercambiando mensajes
