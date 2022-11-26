<template>
  <div class="container">
    <h3 class="">Child component 2</h3>
    <span>Click the below button for example of child to parent using Emit</span>
    <br>
    <button class="mt-5 btn btn-primary" @click="performEmit">Click me!</button>
  </div>
</template>

<script>
export default {
  name: 'HelloWorld',
  props: {
    childParent: Function
  },
  data() {
    return{
      emited_Data: "This is emit example"
    }
  },
  methods:{
    performEmit(){
      this.$emit('emitExample', this.emited_Data);
    }
  }
}
</script>
