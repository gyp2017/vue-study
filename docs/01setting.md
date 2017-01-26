# 1 설정

## 0 준비사항
- [webpack-study](https://github.com/gyp2017/webpack-study) 참고
- [yarn](https://yarnpkg.com/) 참고
- [webpack 2](https://webpack.js.org/) 참고


## 1.1 Creating a new project
`package.json` 파일 생성
```sh
$ yarn init
```

## 1.2 webpack2 설치
```sh
$ yarn add webpack@beta --dev
```

## 1.3 webpack2 설정
`webpack.config.js` 파일 작성
```js
module.exports = {
  entry: './src/app.js',
  output: {
    filename: 'bundle.js',
    path: './dist'
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
