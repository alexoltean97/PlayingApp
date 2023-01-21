<template>
  <h1>Register</h1>
  <h3>A company Id will be generated automatically</h3>
  <form @submit.prevent="submitForm()">

      <div>
        <label for="companyEmail">Company Email</label>
        <input type="text" v-model="email" id="companyEmail" class="form-control">
        <span v-if="errorMessage" class="error">{{errorMessage}}</span>
      </div>

      <div>
          <label for="companyName">Company Name</label>
          <input type="text" v-model="companyName"  id="companyName" class="form-control"/>
          <span v-if="companyError" class="error">{{companyError}}</span>
      </div>


      <div>
          <label for="password">Password</label>
          <input type="password" v-model="password" id="password" class="form-control"/>
          <span v-if="passError" class="error">{{ passError }}</span>
      </div>

    <button type="submit">Register</button>
  </form>
</template>

<script>
export default {
  name: "RegisterMain",
    data(){
      return{
          companyName: '',
          companyError: '',
          email: '',
          errorMessage:'',
          password: '',
          passError: ''
      }
    },

    watch:{

      email: function () {
          this.validateEmail()
      },

        companyName:function (){
          this.validateCompany()
        },

      password: function (){
        this.validatePassword()
      }
    },

    methods: {

      submitForm(){
          this.validateEmail()
          this.validateCompany()
          this.validatePassword()
          if (!this.errorMessage && !this.passError && !this.companyError) {
              console.log("Form Submitted Successfully")
          } else {
              console.log("Form contains errors")
          }
      },

      validateCompany(){
          if(!this.companyName){
              this.companyError = 'Company name is required.'
              return
          }

          this.companyError = ''
      },

      validateEmail(){
          if(!this.email){
              this.errorMessage = 'Email is required.'
              return
          }
          const re = /^\w+([.-]?\w+)*@\w+([.-]?\w+)*(\.\w{2,3})+$/
          if(!re.test(this.email)){
              this.errorMessage = 'Please enter a valid email address.'
              return
          }
          this.errorMessage = ''
      },

      validatePassword(){
          if(!this.password){
              this.passError = 'Password is required.'
              return
          }

          if(this.password < 10){
              this.passError = "Password can't be smaller than 10 characters"
              return
          }

          if (!/\d/.test(this.password)) {
              this.passError = 'Password must contain at least one digit.'
              return
          }

          if (!/[A-Z]/.test(this.password)) {
              this.passError = 'Password must contain at least one uppercase letter.'
              return
          }
          this.passError = ''
      }
    }
}
</script>

<style scoped>
div{
    margin-bottom: 25px;
}
</style>
