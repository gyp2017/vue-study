# 1 설정

## 0 준비사항
- [webpack-study](https://github.com/gyp2017/webpack-study) 참고
- [yarn - workflow](https://yarnpkg.com/en/docs/yarn-workflow) 참고
- [webpack2 - Getting Started](https://webpack.js.org/get-started/) 참고


## 1.1 Creating a new project
`package.json` 파일 생성
```sh
$ yarn init
```

## 1.2 webpack2 설치
```sh
$ yarn add webpack@beta --dev
```

`package.json` 파일 확인
```json
{
  ...
  "devDependencies": {
    "webpack": "beta"
  }
}
```

## 1.3 webpack2 설정
`webpack.config.js` 파일 작성
```js
const path = require('path');

module.exports = {

  entry: './src/main.js',

  output: {
    path: path.resolve(__dirname, 'dist'),
    filename: 'bundle.js'
  }

}
```

## 1.4 scripts 설정
`package.json` 파일 수정
```json
{
  ...
  "scripts": {
    "server": "python -m SimpleHTTPServer 8000",
    "bundle": "webpack"
  },
  ...
}
```
