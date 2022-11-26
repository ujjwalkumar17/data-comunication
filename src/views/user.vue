<template>
  <div class="container">
    <h3 class="">Child component 1</h3>
    <span>Click the below button for example of child to parent using pros</span>
    <br>
    <button class="mt-5 btn btn-primary" @click="childParent(message)">Click me!</button>
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
      message: 'My name is ujjwal and this is the example of child to parent communication',
    }
  }
}
</script>
