<template>
        <form @submit.prevent="handleSubmit">
                <h2>{{ title }}</h2>
                <CustomLoginInput
                        class="input"
                        type="email"
                        :label="emailLabel"
                />
                <CustomLoginInput
                        class="input"
                        type="password"
                        :label="passwordLabel"
                />
                <button>Log in</button>
        </form>
</template>

<script>
import CustomLoginInput from "../components/CustomLoginInput";
export default {
        name: "Login",
        components: { CustomLoginInput },
        data() {
                return {
                        title: "Login",
                        email: "",
                        password: "",
                        emailLabel: "Email",
                        passwordLabel: "Password",
                };
        },
        methods: {
                handleSubmit() {
                        console.log(this.email, this.password);
                },
        },
};
</script>

<style scoped>
.input {
        margin: 10px;
        display: block;
}
</style>
