---
title: Generator
slug: Web/JavaScript/Reference/Global_Objects/Generator
page-type: javascript-class
browser-compat: javascript.builtins.Generator
sidebar: jsref
---

The **`Generator`** object is returned by a {{jsxref("Statements/function*", "generator function", "", 1)}} and it conforms to both the [iterable protocol](/en-US/docs/Web/JavaScript/Reference/Iteration_protocols#the_iterable_protocol) and the [iterator protocol](/en-US/docs/Web/JavaScript/Reference/Iteration_protocols#the_iterator_protocol).

`Generator` is a subclass of the hidden {{jsxref("Iterator")}} class.

## Constructor

There's no JavaScript entity that corresponds to the `Generator` constructor. Instances of `Generator` must be returned from [generator functions](/en-US/docs/Web/JavaScript/Reference/Statements/function*):

```js
function* generator() {
  yield 1;
  yield 2;
  yield 3;
}

const gen = generator(); // "Generator { }"

console.log(gen.next().value); // 1
console.log(gen.next().value); // 2
console.log(gen.next().value); // 3
```

There's only a hidden object which is the prototype object shared by all objects created by generator functions. This object is often stylized as `Generator.prototype` to make it look like a class, but it should be more appropriately called {{jsxref("GeneratorFunction.prototype.prototype")}}, because `GeneratorFunction` is an actual JavaScript entity. To understand the prototype chain of `Generator` instances, see {{jsxref("GeneratorFunction.prototype.prototype")}}.

## Instance properties

These properties are defined on `Generator.prototype` and shared by all `Generator` instances.

- {{jsxref("Object/constructor", "Generator.prototype.constructor")}}
  - : The constructor function that created the instance object. For `Generator` instances, the initial value is [`GeneratorFunction.prototype`](/en-US/docs/Web/JavaScript/Reference/Global_Objects/GeneratorFunction).

    > [!NOTE]
    > `Generator` objects do not store a reference to the generator function that created them.

- `Generator.prototype[Symbol.toStringTag]`
  - : The initial value of the [`[Symbol.toStringTag]`](/en-US/docs/Web/JavaScript/Reference/Global_Objects/Symbol/toStringTag) property is the string `"Generator"`. This property is used in {{jsxref("Object.prototype.toString()")}}.

## Instance methods

_Also inherits instance methods from its parent {{jsxref("Iterator")}}_.

- {{jsxref("Generator.prototype.next()")}}
  - : Returns a value yielded by the {{jsxref("Operators/yield", "yield")}} expression.
- {{jsxref("Generator.prototype.return()")}}
  - : Acts as if a `return` statement is inserted in the generator's body at the current suspended position, which finishes the generator and allows the generator to perform any cleanup tasks when combined with a [`try...finally`](/en-US/docs/Web/JavaScript/Reference/Statements/try...catch#the_finally_block) block.
- {{jsxref("Generator.prototype.throw()")}}
  - : Acts as if a `throw` statement is inserted in the generator's body at the current suspended position, which informs the generator of an error condition and allows it to handle the error, or perform cleanup and close itself.

## Examples

### An infinite iterator

With a generator function, values are not evaluated until they are needed. Therefore a generator allows us to define a potentially infinite data structure.

```js
function* infinite() {
  let index = 0;

  while (true) {
    yield index++;
  }
}

const generator = infinite(); // "Generator { }"

console.log(generator.next().value); // 0
console.log(generator.next().value); // 1
console.log(generator.next().value); // 2
// …
```

## Specifications

{{Specifications}}

## Browser compatibility

{{Compat}}

## See also

- {{jsxref("Statements/function*", "function*")}}
- [`function*` expression](/en-US/docs/Web/JavaScript/Reference/Operators/function*)
- {{jsxref("GeneratorFunction")}}
- [Iteration protocols](/en-US/docs/Web/JavaScript/Reference/Iteration_protocols)
