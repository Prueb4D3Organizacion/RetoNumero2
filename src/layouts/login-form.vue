<script setup>
import { ref } from 'vue'
import RegisterForm from './register-form.vue'

const username = ref('')
const password = ref('')
const userType = ref('')
const butonLogin = ref('')
const butonSwitchRegister = ref(false)
</script>

<template>
  <div v-if="butonSwitchRegister">
    <RegisterForm />
  </div>
  <div v-else>
    <h2>Login</h2>
    <label for = "username">Username: </label>
    <input v-model="username" type="text" id="username"><br><br>
    <label for = "password">Password: </label>
    <input v-model="password" type = "password" id="password"><br><br>
    <label>User Type: </label>
    <input v-model = "userType" type = "radio" value = "Usuario" id="user">
    <label for = "user">Usuario</label>
    <input v-model="userType" type="radio" value="Administrador" id="admin">
    <label for = "admin">Administrador</label><br><br>
    <button @click="butonLogin">Login</button><br><br>
    <button @click ="butonSwitchRegister = ! butonSwitchRegister">Switch to Register</button>
  </div>
</template>

<style scoped>

</style>