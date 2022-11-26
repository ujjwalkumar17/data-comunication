<template>
  <div class="home">
    <img alt="Vue logo" src="../assets/logo.png">
    <HelloWorld msg="Welcome to Your Vue.js App" example="This is the example of parent to child data transfer"/>
    <user />
  </div>
</template>

<script>
// @ is an alias to /src
import HelloWorld from '@/components/HelloWorld.vue'

export default {
  name: 'HomeView',
  data(){
    return{
      name: ''
    }
  },
  components: {
    HelloWorld
  },
}
</script>
