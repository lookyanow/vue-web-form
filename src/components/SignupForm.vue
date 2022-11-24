<template>
  <form @submit.prevent="handleSubmit">
    <label>Email:</label>
    <input type="email" required v-model="email">

    <label>Password:</label>
    <input type="password" required v-model="password">

    <label>Role:</label>
    <select v-model="role">
        <option value="developer">Web developer</option>
        <option value="designer">Web designer</option>
    </select>
    <button type="submit">Create account</button>
  </form>

  <p>Email: {{ email }}</p>
  <p>Password: {{ password }}</p>
  <p>Role: {{ role }}</p>
</template>

<script>
export default {
    data(){
        return{
            email: '',
            password: '',
            role: 'designer',
        }
    },
    methods:{
      handleSubmit(){
        console.log('submit happend')
      }
    }
}
</script>

<style>

</style>