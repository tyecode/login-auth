<template>
    <div class="login-form">
        <h1>Login</h1>
        <form @submit.prevent="handleSubmit">
            <input 
                type="text" 
                placeholder="Username"
                v-model="username"
                required
            />
            <input 
                type="password" 
                placeholder="Password"
                v-model="password"
                required
            />
            <button type="submit">Login</button>
            <p class="error-message">{{errorMessage}}</p>
        </form>
    </div>
</template>

<script>
export default {
    name: "LoginForm",
    data() {
        return {
            username: '',
            password: '',
            errorMessage: '',
        }
    },
    methods: {
        handleSubmit() {
            if(this.username == "user" && this.password == "user") {
                this.$router.push('/UserPage')
            } else if(this.username == "admin" && this.password == "admin") {
                this.$router.push('/AdminPage')
            } else {
                this.errorMessage = "Your username or password is incorrect."
            }
        }
    }
}
</script>