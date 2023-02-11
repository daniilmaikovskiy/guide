- что такое React и зачем нужен
- React Fiber engine (по-моему уже не очень хорошо говорить что главная фича React это Virtual DOM, на мой взгляд это все-таки Fiber если речь про 16 версию и выше) [link](https://blog.logrocket.com/deep-dive-react-fiber/#what-react-fiber) - обычно не нужно глубоко понимать а достаточно знать что это такое
- что такое Компонент, что такое Элемент
- что выведет консоль
```
console.log(<div>hi</div>);
```
- хуки useState, useEffect
- что выведет консоль при заданных событиях
```
//  события
// 1. монтирование
// 2. изменился props.a
// 3. изменился props.b
// 4. размонтирование
const Comp = (props) => {
	console.log('1');

	useEffect(() => {
		console.log('2');

		return () => { console.log('3'); };
	}, [props.b]);

	return null;
}

```
- отличие componentDidMount, useEffect и useLayoutEffect
- React.memo, что делает второй аргумент у React.memo
- паттерны переиспользования кода в React
- как сделать рендер в браузере в обход рендера React? (Ответ - использовать ref, вызвать нативный браузерный API)
- Алгоритм [Reconciliation](https://ru.reactjs.org/docs/reconciliation.html)
- Новые фичи React, начиная с React 16 по 18 ([React docs](https://reactjs.org)) (делаете особый акцент на auto-batching, [useTransition и useDeferredValue](https://youtu.be/QfIwLDy8j_U)), что [завезли](https://github.com/facebook/react/blob/main/CHANGELOG.md) в реакт начиная с 16 версии

- [Redux Toolkit](https://redux-toolkit.js.org/), Redux Toolkit Query (особенно метод [createApi](https://redux-toolkit.js.org/rtk-query/overview#apis))
- (Дополнительно) Посмотреть [мою кастомную реализацию createApi со стабами](https://github.com/danimaik/black-wall-group/blob/master/src/components/service.js)
