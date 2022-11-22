<template>
  <LoginForm />
</template>

<style>
@import '../assets/styles/main.css';
</style>

<script>
import LoginForm from '../components/LoginForm.vue';

export default {
    name: "IndexPage",
    components: { 
      LoginForm, 
    }
}
</script>
