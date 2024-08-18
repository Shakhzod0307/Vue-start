
<template xmlns="http://www.w3.org/1999/html">
<!--  <button style="padding: 10px 30px; color:red; font-size: 25px" @click="count++">{{ count }}</button>-->
<!--  <button @click="clickMe">Click Me</button>-->
  <h1>{{name}} </h1>
  <p style="color: green" v-if="status==='Active'">User is Online</p>
  <p style="color: blue" v-else-if="status==='Pending'">User is Pending</p>
  <p style="color: red" v-else>User is Offline</p>
  <h3 >Tasks:</h3>

  <ul>
    <li v-for="task in tasks" :key="task">{{task}}</li>
  </ul>
<!--  <a style="color: green; " :href="link">Click for Google</a>-->
  <button @click="ChangeStatus">Change Status</button>
  <hr>
<!--  <form @submit.prevent="AddTask">-->
<!--      <label for="newTask">Add Task</label>-->
<!--      <input type="text" id="newTask" name="newTask" v-model="newTask">-->
<!--    <button type="submit">Submit</button>-->
<!--  </form>-->

</template>

<script>
export default {
  data() {
    return {
      count: 1,
      name: "Jack",
      status: "Active",
      tasks: ['Task one','Task two','Task three'],
      link: "https://google.com",

    };
  },
  methods:{
    clickMe(){
      console.log('Clicked');
      this.message = "Updated";
    },
    ChangeStatus(){
      if (this.status ==="Active"){
        this.status = "Pending"
      } else if(this.status ==="Pending"){
        this.status = "Offline"
      } else{
        this.status = "Active"
      }

    },

  },
  computed: {
    now(){
      return Date.now()
    }
  },
};

</script>


<style scoped>

</style>
