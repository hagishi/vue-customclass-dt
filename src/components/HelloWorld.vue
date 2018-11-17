<template>
  <div class="hello">
    {{ foo.dt }}
  </div>
</template>

<script lang="ts">
import { Component, Prop, Vue } from 'vue-property-decorator';
import Fuji from '@/Fuji';

@Component
export default class HelloWorld extends Vue {
  @Prop() private msg!: string;
  @Prop() private foo!: Fuji;
  public created() {
    console.log(this.foo.dt);
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
h3 {
  margin: 40px 0 0;
}
ul {
  list-style-type: none;
  padding: 0;
}
li {
  display: inline-block;
  margin: 0 10px;
}
a {
  color: #42b983;
}
</style>
