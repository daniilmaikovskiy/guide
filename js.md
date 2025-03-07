### JS
- отличие ECMAScript от JavaScript
- Типы данных (8 шт)
- JSON (что это, что нельзя конвертировать в JSON)
- назвать 6 типов данных JSON
- [замыкание](https://ru.wikipedia.org/wiki/%D0%97%D0%B0%D0%BC%D1%8B%D0%BA%D0%B0%D0%BD%D0%B8%D0%B5_(%D0%BF%D1%80%D0%BE%D0%B3%D1%80%D0%B0%D0%BC%D0%BC%D0%B8%D1%80%D0%BE%D0%B2%D0%B0%D0%BD%D0%B8%D0%B5))
- какие новые фичи вышли в ECMAScript 2022
- методы массивов, нужно сказать какие мутируют, какие нет
- мутирует ли Array.prototype.sort
- разница между ключами Object.keys и ключами из цикла for in
- разница между var, let и const
- как отработает код и почему, как это исправить
```
for (var i = 0; i < 10; i++) {
  setTimeout(() => {
    console.log(i);
  }, 0);
}
```
- контекст вызова this. Как ведет себя в стрелочной и обычной функции
- Что выведет консоль и почему
```
const user = {
  name: 'Bob',
  funcFunc() {
    return function() {
      console.log(this);
    }
  },
  funcArrow() {
    return () => {
      console.log(this);
    }
  },
  arrowFunc: () => {
    return function() {
      console.log(this);
    }
  },
  arrowArrow: () => {
    return () => {
      console.log(this);
    }
  },
};

user.funcFunc()();
user.funcArrow()();
user.arrowFunc()();
user.arrowArrow()();
```
- Что выведет консоль и почему
```
const user2 = {
  name: 'Jim',
  funcFunc: user.funcFunc(),
  funcArrow: user.funcArrow(),
  arrowFunc: user.arrowFunc(),
  arrowArrow: user.arrowArrow()
}

user2.funcFunc();
user2.funcArrow();
user2.arrowFunc();
user2.arrowArrow();
```
- что такое асинхронность, определение
- микро и макро таски
- как отработает код и почему
```
console.log(1);
setTimeout(() => {
  console.log(2);
}, 0);
const myPromise = new Promise((resolve, reject) => {
  console.log(3);
  resolve(4);
}).then((value) => console.log(value));
console.log(5);
```
```
new Promise((resolve) => {
  console.log("Message 0");
});

console.log("Message 1");

setTimeout(() => console.log("Message 2"));

Promise.resolve()
  .then(() => console.log("Message 3"))
  .then(() => setTimeout(() => console.log("Message 4")));
  
setTimeout(() => console.log("Message 5"));

console.log("Message 6");
```

- Как устроено наследование
- Что выведет консоль и почему
```
// 1.
console.log(({}).prototype === ({}).__proto__);
// 2. 
function Func() {};
console.log(Func.prototype === Func.__proto__);
// 3-4.
function Func1() {};
function Func2() {};
console.log(Func1.__proto__ === Func2.__proto__);
console.log(Func1.prototype === Func2.prototype);
// 5.
let Component = (props) => {
  return `<div>I don't know Prototype</div>`;
};
console.log(Component.prototype === Object.prototype);
// 6-7.
let age = 18;
console.log(age.prototype === Number.prototype);
console.log(age.__proto__ === Number.prototype);
// 8.
class Hacker {}
console.log(Hacker.__proto__ === Function.prototype);
```

### TypeScript (если хочется указать его в резюме)

- Типы данных
- Дженерики, union-types
- Utility types (особенно Record, ReturnType, Partial, Omit)
- Как написать подобие Record при помощи interface
- (Дополнительно) infer
