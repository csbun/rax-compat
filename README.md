# rax-compat

This module makes React-based modules work with [Rax](https://alibaba.github.io/rax/)(web), without any code changes.

## Installation

You need to install rax-compat first through npm:

```
npm i -S rax-compat
```

And have Rax already installed. If you don't, install it like:

```
npm i -S rax
```

Or with yarn:

```
yarn add rax-compat rax
```

## Usage with Webpack

Add an alias for react and react-dom:

```javascript
{
  resolve: {
    alias: {
      'react': 'rax-compat',
      'react-dom': 'rax-compat',
    }
  },
}
```

If you are using [babel-preset-rax](https://www.npmjs.com/package/babel-preset-rax), you should overwrite plugin [babel-plugin-transform-react-jsx](https://www.npmjs.com/package/babel-plugin-transform-react-jsx) in _.babelrc_ (or babel-loader in _webpack.config.js_) with default config.

```json
{
  "plugins": [ "transform-react-jsx" ]
}
```
