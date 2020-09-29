<template>
  <div id="app">
    <div :class="classObject">{{ value }}</div>

    <button type="button" @click="value++">+</button>
    <button type="button" @click="value--">-</button>
    <!-- <button type="button" @click="error = ! error">error</button> -->
    <!-- <button type="button" @click="warning = ! warning">warning</button> -->
  </div>
</template>

<script>
// import HelloWorld from './components/HelloWorld.vue'

  export default {
    name: 'app',

    data: function () {
      return {
        value: 8,
        error: false,
        warning: false,
      }
    },

    computed: {
      classObject: function () {
        return {
        'red-error' : this.value >= 10, 
        // 'normal-green': 5 < this.value < 10,
        'yellow-warning' : this.value <= 5,
        }
      }
    }
  }
</script>

<style>
  body {
    font-size: 40px;
    text-align: center;
    padding-top: 100px;
  }

  .red-error {
    background-color: darkred;
  }

  .yellow-warning {
    background-color: yellow;
  }

  .normal-green{
    background-color: green;
  }
</style>
