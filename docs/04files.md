# 4 files

## 4.1 `./index.html`
```html
<!DOCTYPE html>
<html>
  <head>
    <meta charset="utf-8">
    <title></title>
  </head>
  <body>
    <div id="app">
      <!-- 여기에 앱 컴포넌트!! -->
    </div>

    <script src="./dist/bundle.js" charset="utf-8"></script>
  </body>
</html>
```

## 4.2 `./components/App.vue`
- [language-vue](https://atom.io/packages/language-vue)

```html
<template lang="html">
  <div class="app">
    <h1>{{ greeting }}</h1>
  </div>
</template>

<script>
export default {
  data() {
    return {
      greeting: 'Hi Hello'
    }
  }
}
</script>

<style lang="css">
.app {
  background-color: pink;
}
</style>
```

## 4.3 `./main.js`
```js
import Vue from 'vue'
import App from './components/App.vue'

new Vue({
  el: '#app',
  render: h => h(App)
})
```
