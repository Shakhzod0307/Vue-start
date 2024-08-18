
<template>
  <button style="padding: 10px 30px; color:red; font-size: 25px" @click="count++">{{ count }}</button>
  <h1>{{message}}</h1>
  <button @click="clickMe">Click Me</button>
</template>

<script>
export default {
  data() {
    return {
      count: 1,
      message: "Hello",
    };
  },
  methods:{
    clickMe(){
      console.log('Clicked');
      this.message = "Updated";
    }
  }
};

</script>


<style scoped>

</style>
