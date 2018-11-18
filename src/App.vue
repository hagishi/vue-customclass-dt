<template>
  <div id="app">
    <img alt="Vue logo" src="./assets/logo.png">
    <div v-for="(foo, i) in foos" :key="i">
      <HelloWorld :foo="foo" msg="Welcome to Your Vue.js + TypeScript App" />
    </div>
  </div>
</template>

<script lang="ts">
import { Component, Vue } from 'vue-property-decorator';
import HelloWorld from './components/HelloWorld.vue';
import Fuji from './Fuji';

@Component({
  components: {
    HelloWorld,
  },
})
export default class App extends Vue {
  public foos = [new Fuji(new Date()), new Fuji(new Date())];
}
</script>

<style>
#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
