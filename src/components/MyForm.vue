<template>
  <form @submit.prevent="onSubmit">
    <label for="name">Name:</label>
    <input v-model="form.name" type="text" id="name" required />

    <label for="email">Email:</label>
    <input v-model="form.email" type="email" id="email" required />

    <label for="password">Password:</label>
    <input v-model="form.password" type="password" id="password" required minlength="8" />

    <label for="confirmPassword">Confirm Password:</label>
    <input v-model="form.confirmPassword" type="password" id="confirmPassword" required minlength="8" />

    <label for="newsletter">
      <input v-model="form.newsletter" type="checkbox" id="newsletter" />
      Subscribe to newsletter
    </label>

    <button type="submit" :disabled="form.password !== form.confirmPassword">Sign Up</button>
  </form>
</template>

<script>
export default {
  data() {
    return {
      form: {
        name: '',
        email: '',
        password: '',
        confirmPassword: '',
        newsletter: false,
      },
    };
  },
  methods: {
    onSubmit() {
      // handle form submission
    },
  },
};
</script>


<style>
input[ type="text"]{
  padding: 20px;
  margin-bottom: 0.4ch;
}

button[type="submit"]{
  padding: 20px;
  margin-top: 0.4ch;
  background-color: rgb(242, 15, 15);
  color: rgb(244, 16, 206);
}
</style>