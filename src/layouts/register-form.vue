<script setup>
import LoginForm from './login-form.vue'
import { ref } from 'vue'
const username = ref('')
const email = ref('')
const password = ref('')
const confirmPassword = ref('')
const userType = ref('')
const butonRegister = ref('')
const butonSwitchLogin = ref(false)
</script>

<template>
  <div v-if="butonSwitchLogin">
    <login-form/>
  </div>
  <div v-else>
    <h2>Register</h2>
    <label for="username">Username: </label>
    <input v-model="username" type="text" id="username"><br><br>
    <label for="email">Email: </label>
    <input v-model="email" type="email" id="email"><br><br>
    <label for="password">Password: </label>
    <input v-model="password" type="password" id="password"><br><br>
    <label for="confirmPassword">Confirm Password: </label>
    <input v-model="confirmPassword" type="password" id="confirmPassword"><br><br>
    <label>User Type: </label>
    <input v-model="userType" type="radio" value="Usuario" id="user">
    <label for="user">Usuario</label>
    <input v-model="userType" type="radio" value="Administrador" id="admin">
    <label for="admin">Administrador</label><br><br>
    <button @click="butonRegister">Register</button><br><br>
    <button @click="butonSwitchLogin = ! butonSwitchLogin">Switch to Login</button>
  </div>

</template>

<style scoped>

</style>