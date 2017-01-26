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
