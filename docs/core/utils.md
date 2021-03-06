---
title: Utils
type: core
layout: docs
parent_section: core
order: 10
---

Most of A-Frame's utility modules are public through `AFRAME.utils`.

<!--toc-->

## AFRAME.utils.coordinates

Module for handling vec3 and vec4 types.

### .isCoordinate(value)

Tests whether a string is a vec3.

```js
AFRAME.utils.coordinates.isCoordinate('1 2 3')
// >> true
```

### .parse(value)

Parses an "x y z" string to an `{x, y, z}` vec3 object. Or parses an "x y z w" string to an {x, y, z w} vec3 object.

```js
AFRAME.utils.coordinates.parse('1 2 -3')
// >> {x: 1, y: 2, z: -3}
```

### .stringify(data)

Stringifies an `{x, y, z}` vec3 object to an "x y z" string.

```js
AFRAME.utils.coordinates.stringify({x: 1, y: 2, z: -3})
// >> "1 2 -3"
```

## AFRAME.utils.styleParser

### .parse(value)

Parses a CSS style-like string to an object.

```js
AFRAME.utils.styleParser.parse('attribute: color; dur: 5000;')
// >> {"attribute": "color", "dur": "5000"}
```

### .stringify(data)

Stringifies an object to a CSS style-like string.

```js
AFRAME.utils.styleParser.stringify({height: 10, width: 5})
// >> "height: 10; width: 5"
```

## Object Utils

### deepEqual(a, b)

Checks if two objects have the same attributes and values, including nested objects.

```
deepEqual({a: 1, b: {c: 3}}, {a: 1, b: {c: 3}})
// >> true
```

### diff(a, b)

Returns difference between two objects. The returned object's set of keys denote which values were not equal, and the set of values are `b`'s values.

```js
diff({a: 1, b: 2, c: 3}, {b: 2, c: 4})
// >> {"a": undefined, "c": 4}
```

### extend(target, source, [source, ...])

[Object Assign polyfill](https://www.npmjs.com/package/object-assign)

### extendDeep(target, source, [source, ...])

[Deep Assign](https://www.npmjs.com/package/deep-assign)
