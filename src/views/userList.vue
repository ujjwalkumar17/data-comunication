<template>
  <div class="container">
    <!-- {{userList}} -->
    <div class="card p-3">
      <table class="table table-striped hover" id="userListTable">
      <thead class="thead-dark">
        <tr>
          <th scope="col">S. no.</th>
          <th scope="col">Name</th>
          <th scope="col">Email</th>
          <th scope="col">Mobile</th>
        </tr>
      </thead>
      <tbody class="text-left">
        <tr v-for="(user, index) in userList" :key="user.id">
          <th scope="row">{{Number(index + 1)}}</th>
          <td>{{user.name}}</td>
          <td>{{user.email}}</td>
          <td>{{user.phone}}</td>
        </tr>
      </tbody>
    </table>
    </div>
  </div>
</template>

<script>
import axios from 'axios'
export default {
  name: 'HelloWorld',
  data() {
    return{
      userList: {}
    }
  },
  props: {
    msg: String
  },
  created(){
    this.userData();
  },
  methods:{
    async userData(){
      try{
        // console.log('hello')
        let res= await axios.get('https://jsonplaceholder.typicode.com/users')
        this.userList=res.data

        $(document).ready(function () {
            $('#userListTable').DataTable();
        });
      }catch(err){
        console.log(err);
      }
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
div#userListTable_length {
    text-align: left;
}
</style>
