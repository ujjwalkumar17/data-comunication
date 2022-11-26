<template>
  <div class="container">
    <div class="card p-3 shadow">
      <form>
        <div class="form-row row">
          <div class="form-group mb-2 col-md-6">
            <label>Name</label>
            <input 
              v-model="name"
              type="name"
              class="form-control"
              required
              placeholder="name"
            />
          </div>
          <div class="form-group mb-2 col-md-6">
            <label>Email</label>
            <input 
              v-model="email"
              type="email"
              class="form-control"
              required
              placeholder="Email"
            />
          </div>
          <div class="form-group mb-2 col-md-12">
            <label>Mobile</label>
            <input 
              v-model="mobile"
              type="number"
              class="form-control"
              required
              placeholder="Mobile"
            />
          </div>
        </div>
        <button @click="addUser()" class="btn btn-primary">Sign in</button>
      </form>
    </div>
  </div>
</template>

<script>
import { mapGetters } from "vuex";
import { mapActions } from "vuex";

export default {
  name: "Form",
  data() {
    return {
      name: '',
      email: '',
      mobile: '',
    };
  },
  computed: {
    ...mapGetters([
    ]),
  },
  created() {},
  methods: {
    addUser(){
      let user = {
        name : this.name,
        email : this.email,
        mobile : this.mobile,
      }
      // console.log(user)
      
    }
  },
};
</script>


