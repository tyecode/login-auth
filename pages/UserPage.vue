<template>
    <div class="wrapper">
        <Navbar />
        <h1 class="content">Welcome to <span>User</span> Page</h1>
    </div>
</template>

<style>
@import '../assets/styles/main.css';
</style>

<script>
import Navbar from '../components/Navbar.vue';

export default {
    name: "UserPage",
    components: { Navbar },
}
</script>