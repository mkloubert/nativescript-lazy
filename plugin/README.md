# Nativescript Lazy

A [NativeScript](https://nativescript.org/) module that provides an OOP version of the build-in lazy function.

## NativeScript Toolbox

This module is part of [nativescript-toolbox](https://github.com/mkloubert/nativescript-toolbox).

## License

[MIT license](https://raw.githubusercontent.com/mkloubert/nativescript-lazy/master/LICENSE)

## Platforms

* Android
* iOS

## Installation

Run

```bash
tns plugin add nativescript-lazy
```

inside your app project to install the module.

## Example

```typescript
import { Lazy } from require('nativescript-lazy');

var lazyValue = new Lazy<Date>(() => new Date());

// [1] (false)
console.log('isValueCreated: ' + lazyValue.isValueCreated);
// [2] current time
console.log('value: ' + lazyValue.value);
// [3] (true)
console.log('isValueCreated: ' + lazyValue.isValueCreated);
// [4] same value from [2]
console.log('value: ' + lazyValue.value);

lazyValue.reset();

// [5] (false)
console.log('isValueCreated: ' + lazyValue.isValueCreated);
// [6] (new) current time
console.log('value: ' + lazyValue.value);
// [7] (true)
console.log('isValueCreated: ' + lazyValue.isValueCreated);
// [8] same value from [6]
console.log('value: ' + lazyValue.value);
```
