<template>
  <div class="container">
    <div class="card p-5">
      <h1>{{msg}}</h1>
    <p>{{example}}</p>
    </div>
    <hr>
    <div class="card shadow p-3" style="height:200px">
      <childOne :childParent="getUser"/>
    </div>
    <hr>
    <div class="card shadow p-3" style="height:200px">
      <childTwo @emitExample="newEmitedData"/>
    </div>
  </div>
</template>

<script>
import childOne from "@/views/user.vue"
import childTwo from "@/views/emitExample.vue"
export default {
  name: 'HelloWorld',
  props: {
    msg: String,
    example: String,
  },
  components:{
    childOne,
    childTwo
  },
  methods:{
    getUser(name){
      alert(name);
    },
    newEmitedData(emitExample){
      alert(emitExample)
    }
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
