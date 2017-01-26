# 2 vue 설치

## 0 준비사항
- [vue installation](https://vuejs.org/v2/guide/installation.html) 참고
- [vue installation 한글](https://kr.vuejs.org/v2/guide/installation.html) 참고

## 2.1 vue
```sh
$ yarn add vue
```

`package.json` 파일 확인
```json
{
  ...
  "dependencies": {
    "vue": "^2.1.10"
  }
}
```

## 2.2 vue-loader
- [vue-loader](https://vue-loader.vuejs.org/en/)
- [vue-loader 한글](https://vue-loader.vuejs.org/kr/)

```sh
$ yarn add vue-loader --dev
```

```sh
yarn add v0.19.1
[1/4] 🔍  Resolving packages...
[2/4] 🚚  Fetching packages...
[3/4] 🔗  Linking dependencies...
warning "vue-loader@10.0.3" has unmet peer dependency "css-loader@*".
warning "vue-loader@10.0.3" has unmet peer dependency "vue-template-compiler@^2.0.0".
[4/4] 📃  Building fresh packages...
success Saved lockfile.
success Saved 28 new dependencies.
```

- [css-loader](https://github.com/webpack-contrib/css-loader)
```sh
$ yarn add css-loader --dev
```

- [vue-template-compiler](https://www.npmjs.com/package/vue-template-compiler)
```sh
$ $ yarn add vue-template-compiler --dev
```

`webpack.config.js` 파일 수정
```js
  ...

  module: {
    rules: [
      {
        test: /\.js$/,
        loader: 'babel-loader',
        exclude: /node_modules/
      },
      {
        test: /\.vue$/,
        loader: 'vue-loader'
      }
    ]
  }

}
```


```sh
yarn run v0.19.1
$ webpack
Hash: c781f680606fac90314d
Version: webpack 2.2.0
Time: 1066ms
    Asset    Size  Chunks             Chunk Names
bundle.js  171 kB       0  [emitted]  main
   [0] ./src/bar.js 109 bytes {0} [built]
   [1] ./~/vue/dist/vue.runtime.common.js 162 kB {0} [built]
   [2] ./~/process/browser.js 5.3 kB {0} [built]
   [3] (webpack)/buildin/global.js 509 bytes {0} [built]
   [4] ./src/main.js 374 bytes {0} [built]
✨  Done in 1.83s.
```

`webpack.config.js` 파일 수정
```js
  ...

  resolve: {
    alias: {
      'vue$': 'vue/dist/vue.common.js'
    }
  }
}
```
