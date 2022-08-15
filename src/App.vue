<template>
  <div id="app">
    <div v-for=""></div>
  </div>
</template>

<script lang="ts">
import axios from 'axios';
import {Vue} from 'vue-property-decorator';

const component = Vue.extend({
    data() {
      return {
        msg:Array([1,2,3,4]),
      }
    },

    methods:{
      getData(){
        axios
          .get('https://api.staging.umeu.app/test/tasks/search?pagingCount=5&pagingAfter=0')
          .then(test=>this.msg = test)
      }

    }
  }
)

export default class App extends Vue {
}

</script>

<style lang="scss">
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
