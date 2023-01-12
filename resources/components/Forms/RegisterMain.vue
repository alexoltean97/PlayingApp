<template>
  <h1>Register</h1>
  <h3>A company Id will be generated automatically</h3>
  <form>
    <label for="company">Company Email</label>
    <input type="text" id="company" class="form-control">
    <label for="companyName">Company Name</label>
    <input type="text" id="companyName" class="form-control"/>
    <label for="password">Password</label>
    <input type="password" id="password" class="form-control"/>
    <button type="submit">Register</button>
  </form>
</template>

<script>
export default {
  name: "RegisterMain"
}
</script>

<style scoped>

</style>