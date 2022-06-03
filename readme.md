# filter-obj

> Filter object keys and values into a new object

## Install

```sh
npm install filter-obj
```

## Usage

```js
import filterObject from 'filter-obj';

const object = {
	foo: true,
	bar: false
};

const newObject = filterObject(object, (key, value) => value === true);
//=> {foo: true}

const newObject2 = filterObject(object, ['bar']);
//=> {bar: false}
```

## API

Symbol keys are not copied over to the new object.

### filterObject(source, filter)
### filterObject(source, includeKeys)

#### source

Type: `object`

The source object to filter properties from.

#### filter

Type: `(sourceKey, sourceValue, source) => boolean`

A predicate function that detemines whether a property should be assigned to the new object.

#### includeKeys

Type: `string[]`

An array of property names that should be assigned to the new object.

## Related

- [map-obj](https://github.com/sindresorhus/map-obj) - Map object keys and values into a new object
