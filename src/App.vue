<template>
  <div id="nav">
    <router-link to="/">Home</router-link> |
    <router-link to="/about">About</router-link> | 
    <router-link :to="{name: 'Jobs'}">Jobs</router-link>
  </div>
  <button @click="redirect" class="btn btn-success mx-3 my-3">Redirect</button>
  <button @click="back" class="btn btn-success mx-3 my-3">Go Back</button>
  <button @click="forward" class="btn btn-success mx-3 my-3">Go Forward</button>
  <router-view/>
</template>
<script>
  import {toRefs, reactive} from 'vue'
  export default{
    setup() {
      const state = reactive({

      });

      return toRefs(state)
    },
    methods: {
      redirect(){},
      back(){
        this.$router.go(-1)
      },
      forward(){
        this.$router.go(+1)
      }
    },
  }
</script>
<style lang="scss">
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
}

#nav {
  padding: 30px;

  a {
    font-weight: bold;
    color: #2c3e50;

    &.router-link-exact-active {
      color: #42b983;
    }
  }
}
</style>
