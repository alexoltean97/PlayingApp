<template>
  <h1>Company Login</h1>
<form>
  <label for="company">Company Email</label>
  <input type="text" id="company" class="form-control">
  <label for="companyId">Company Id</label>
  <input type="text" id="companyId" class="form-control"/>
  <label for="password">Password</label>
  <input type="password" id="password" class="form-control"/>
  <button type="submit">Log in</button>
</form>
</template>

<script>
export default {
  name: "CompanyLogin"
}
</script>

<style scoped>
button{
  margin-top:10px;
}
</style>