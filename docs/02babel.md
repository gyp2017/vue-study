# 2 babel


## 2.1 add babel
- [babel - webpack](https://babeljs.io/docs/setup/#installation)
```sh
$ yarn add babel-core --dev
```

```sh
$ yarn add babel-loader --dev
```

## 2.2 add babel-preset-env
- [babel - Env preset](https://babeljs.io/docs/plugins/preset-env/)
```sh
$ yarn add babel-preset-env --dev
```

`.bablerc` 파일 작성
```json
{
  "presets": ["env"]
}
```


## 2.3 babel 설정
`webpack.config.js` 파일 수정
```js
const path = require('path');

module.exports = {

  entry: './src/main.js',

  output: {
    path: path.resolve(__dirname, 'dist'),
    filename: 'bundle.js'
  },

  module: {
    rules: [
      {
        test: /\.js$/,
        loader: 'babel-loader',
        exclude: /node_modules/
      }
    ]
  }

}
```
