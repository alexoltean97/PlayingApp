<template>
<div class="login-modal">
        <h2>Employee Login</h2>
        <form>
          <label for="employee">Employee Email</label>
          <input type="email" id="employee" class="form-control"/>
          <label for="employee-id">Employee ID</label>
          <input type="text" id="employee-id" class="form-control"/>
          <label for="password">Password</label>
          <input type="password" id="password" class="form-control"/>
          <button type="submit">Log In</button>
        </form>
</div>

</template>

<script>
export default {
  name: "Login"
}
</script>

<style scoped>
button{
  margin-top:10px;
}
</style>