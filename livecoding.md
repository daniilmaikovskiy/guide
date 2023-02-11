1. longestSubstring
```
// Дана строка S, найти подстроку максимальной длины
// Все символы в искомых подстроках идут подряд по строке и
// состоят из уникальных символов

// Пример 1:
// Input: s = "abcabcbb"
// Output: "abc" or "bca" or "cab"

// Пример 2:
// Input: s = "bbbbb"
// Output: "b"

// Пример 3:
Input: s = "pwwkew"
Output: "wke" or "kew"
"pwke" - не верно

*/

function longestSubstring(str = "") {

}

/* testcases */

(function () {
  const s = "pwwkew";
  const result = longestSubstring(s);
  console.log("1", result === "wke" || result === "kew");
})();

(function () {
  const s = "crdghcfrypne";
  console.log("2", longestSubstring(s) === "dghcfrypne");
})();

(function () {
  const s = "crdghfrgrgyanjclxgzuomlqxfgeqguuaxdjcuruapwpbzbyhau";
  console.log("3", longestSubstring(s)?.length === 12);
})();

(function () {
  const s = "hijklmnopqrstuvwxyzABCDEFGHIJKLMNOPQRSTUVWXYZ0123456789hijklmnopqrstuvwxyzABCDEFGHIJKLMNOPQRSTUVWXYZ0123456789hijklmnopqrstuvwxyzABCDEFGHIJKLMNOPQRSTUVWXYZ0123456789hijklmnopqrstuvwxyzABCDEFGHIJKLMNOPQRSTUVWXYZ0123456789hijklmnopqrstuvwxyzABCDEFGHIJKLMNOPQRSTUVWXYZ0123456789hijklmnopqrstuvwxyzABCDEFGHIJKLMNOPQRSTUVWXYZ0123456789";
  console.log("4", longestSubstring(s)?.length === 55);
})();
function longestSubstring(str = "") {

}

/***** testcases *****/

(function () {
  const s = "pwwkew";
  const result = longestSubstring(s);
  console.log("1", result === "wke" || result === "kew");
})();

(function () {
  const s = "crdghcfrypne";
  console.log("2", longestSubstring(s) === "dghcfrypne");
})();

(function () {
  const s = "crdghfrgrgyanjclxgzuomlqxfgeqguuaxdjcuruapwpbzbyhau";
  console.log("3", longestSubstring(s)?.length === 12);
})();

(function () {
  const s = "hijklmnopqrstuvwxyzABCDEFGHIJKLMNOPQRSTUVWXYZ0123456789hijklmnopqrstuvwxyzABCDEFGHIJKLMNOPQRSTUVWXYZ0123456789hijklmnopqrstuvwxyzABCDEFGHIJKLMNOPQRSTUVWXYZ0123456789hijklmnopqrstuvwxyzABCDEFGHIJKLMNOPQRSTUVWXYZ0123456789hijklmnopqrstuvwxyzABCDEFGHIJKLMNOPQRSTUVWXYZ0123456789hijklmnopqrstuvwxyzABCDEFGHIJKLMNOPQRSTUVWXYZ0123456789";
  console.log("4", longestSubstring(s)?.length === 55);
})();
```

***

areValidBrackets2
  
/* Функция принимает строку с комбинацией 
   скобок и возвращает валидна ли она */

function areValidBrackets(str) {
  // Пишите код здесь
}
  
console.log("1", areValidBrackets("(())")); // true
console.log("2", areValidBrackets(")()(")); // false
console.log("3", areValidBrackets("())()(()")); // false
console.log("4", areValidBrackets("(()")); // false
console.log("5", areValidBrackets("(()())()")); // true

function areValidBrackets2(str) {
    // Пишите код здесь
}
    
console.log("1", areValidBrackets2("[](){}")); // true
console.log("2", areValidBrackets2("[{]}")); // false

***

function unpack(arr) {

}
console.log(unpack([1,2,[3,4]])); //[1,2,3,4]
console.log(unpack([ 1,2,3,[ 4,5 ],6,[ 7,[ 8,[9] ] ] ])); //[1,2,3,4,5,6,7,8,9]

***

// дан массив[1, 1, 1, 2, 2, 2, 2, 4, 4, 5, 0]

// Оставить в массиве уникальные элементы
// И отсортировать массив по частоте

const input = [1, 1, 1, 2, 2, 2, 2, 4, 4, 5, 0];

function sortByFrequency (arr = []) {
// code here
}

console.log(sortByFrequency(input));

// response [2, 1, 4, 5, 0] или [2, 1, 4, 0, 5] 

***

function memo(fn) {

}

function plus(a, b) {
  console.log('call', a, b);
  return a + b;
}

const memoPlus = memo(plus);
console.log(memoPlus(1, 2)); // call 1 2 \n 3
console.log(memoPlus(1, 2)); // 3
console.log(memoPlus(3, 1)); // call 3 1 \n 4

plus("3", 1);
console.log(memoPlus("3", 1)); // call 3 1 \n 4

function getA(obj){
  console.log('getA call', obj.a)
  return obj.a
}

const memoGetA = memo(getA);

const a1 = {a: 1}
const a2 = {a: 2}
const a3 = {a: 1}

console.log(memoGetA(a1)); // getA call 1 \n 1
console.log(memoGetA(a2)); // getA call 2 \n 2
console.log(memoGetA(a1)); // 1
console.log(memoGetA(a3)); // 1

***

/* FlatObject
Напишите функцию, которая возвращает новый объект,
в котором все примитивные элементы вложенных объектов были рекурсивно "подняты"(подняты = из вложенного объекта перемещены в текущий) до первого уровня.
Пример:
*/
const obj = {
  a: {
    b: {
      c: 1,
      d: 2,
      e: 3
    },
    f: {
      g: 4,
      h: 5
    }
  },
  i: 6,
  j: 7
};

const flatObject = (obj) => {
  // Пишите свой код сюда
};

console.log(flatObject(obj)) // { c: 1, d: 2, e: 3, g: 4, h: 5, i: 6, j: 7 };

***

/*
PromiseAll
Напишите асинхронную функцию, которая принимает массив промисов и
возвращает массив результатов вызова этих промисов.
Пример:
*/
const firstPromise = new Promise((resolve) =>
  setTimeout(() => resolve(300), 300)
);

const secondPromise = new Promise((resolve) =>
  setTimeout(() => resolve(200), 200)
);

const thirdPromise = new Promise((resolve) =>
  setTimeout(() => resolve(100), 100)
);

const promiseAll = (promisesArr) => {
  return Promise.resolve();
}

promiseAll([firstPromise, secondPromise, thirdPromise]).then(console.log); // [300, 200, 100]

***

/* PromisesInSeries
Напишите функцию, которая принимает массив асинхронных функций и
последовательно(следующая начинается, когда закончилась предыдущая) вызывает их, передавая в аргументы результат вызова предыдущей функции.
Пример:
*/
const firstPromise = () =>
  new Promise((resolve) => setTimeout(() => resolve(300), 300));

const secondPromise = (a) =>
  new Promise((resolve) => setTimeout(() => resolve(a + 200), 200));

const thirdPromise = (b) =>
  new Promise((resolve) => setTimeout(() => resolve(b ** 2), 100));

const promisesInSeries = (promises) => {
  // YOUR CODE HERE
}

promisesInSeries([firstPromise, secondPromise, thirdPromise]).then(console.log);
// (300 + 200) ** 2 = 250 000

***

/* moveToStart
Реализуйте функцию moveToStart, которая принимает массив и число n.
Функция должна переставить n элементов массива из конца в начало.
Если второй аргумент больше или равен
длине массива, то должен быть возвращен новый массив, порядок
элементов которого совпадает с изначальным.
Функция должна возвращать новый массив, а не мутировать старый.
Примеры:
*/
function moveToStart(arr, count) {
  // YOUR CODE HERE
}

console.log(moveToStart([1, 2, 3, 4, 5, 12, 8], 2)); // [12, 8, 1, 2, 3, 4, 5];

console.log(moveToStart([1, 2, 3, 4, 5], 10)); // [1, 2, 3, 4, 5];

***

/*OptionalChaining
Напишите функцию, которая принимает первым параметром объект,
вторым - цепочку свойств, по которой нужно пройти, чтобы получить значение.
Если какое-то из свойств не найдено - функция возвращает undefined.
Пример:
*/
const obj = {
  a: {
    b: {
      c: {
        d: 'Привет!',
      },
    },
  },
};

  
  
function optionalChaining(o, path) {
  // пиши код здесь
};

console.log(optionalChaining(obj, 'a.b.c')); // { d: 'Привет' }
console.log(optionalChaining(obj, 'a.b.c.d')); // Привет
console.log(optionalChaining(obj, 'a.b.c.d.e')); // undefined
console.log(optionalChaining(obj, 'b.d.a')); // undefined
console.log(optionalChaining(obj, '')) /* {
  a: {
    b: {
      c: {
        d: 'Привет!',
      },
    },
  },
} */

***

const user = {
  name: "bob"
};

function bind(context, fn) {
  return function () {};
}

bind(user, function () {
  console.log(this.name);
})();

useDirtyState

import "./styles.css";

// задача: написать кастомный хук useDirtyState
// вначале у которого возвращается isDirty = false
// а если хоть раз применен setState то isDirty = true
// + повесить setState на обработчик клика у increment

const useDirtyState = (initialValue = 0) => {
  return []
};

export default function App() {
  const [state, setState, isDirty] = useDirtyState(0);

  return (
    <div className="App">
      <div>State: {state}</div>
      <div>Is state dirty: {isDirty ? "dirty" : "not dirty"}</div>
      <button>Increment</button>
    </div>
  );
}



















import "./styles.css";


const useWillMount = (callback) => {
 };


export default function App() {
 useWillMount(() => {
   console.log("ok");
 });


 console.log("render");


 return <div className="App"></div>;
}
