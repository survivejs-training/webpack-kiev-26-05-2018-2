# Webpack - The Good Parts

* [Slides](https://presentations.survivejs.com/webpack-the-good-parts/#/1)
* [Book](https://survivejs.com/webpack/)

## Schedule

**26.05.2018**

* 15:30-17:00 - Introduction to webpack.
* 17:00-17:30 - Coffee break?
* 17:30-19:30 - More webpack, freeform in the end?

## Goals

* Learn to maintain webpack configuration.
* How to improve performance of my project.

## Examples

### Loader

```javascript
module.exports = input => input + input;
```

### Plugin

```javascript
class DemoPlugin {
  apply(compiler) {
    ...
  }
}
```

### Resolve

```javascript
import "foo";
```

```javascript
const config = {
  resolve: {
    alias: {
      foo: path.resolve(__dirname, "bar/foo.js"),
    },
    extensions: [
      ".ts", ".js"
    ],
    modules: [
      path.resolve(__dirname, "my_modules"),
      path.resolve(__dirname, "node_modules"),
    ],
  },
};
```
### Loader Order

```javascript
use: ["style-loader", "css-loader"]
```

```javascript
styleLoader(cssLoader(input))
```
