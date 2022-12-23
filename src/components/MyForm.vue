<template>
  <form @submit.prevent="submitForm">
    <label for="name">Name:</label>
    <input v-model="form.name" type="text" id="name" required />
    <br />
    <label for="email">Email:</label>
    <input v-model="form.email" type="email" id="email" required />
    <br />
    <label for="message">Message:</label>
    <textarea v-model="form.message" id="message" required></textarea>
    <br />
    <button type="submit">Send</button>
  </form>
</template>

<script>
export default {
  data() {
    return {
      form: {
        name: "",
        email: "",
        message: ""
      },
      errors: []
    };
  },
  methods: {
    async submitForm() {
      // validate form
      this.errors = [];
      if (!this.form.name) {
        this.errors.push("Name is required.");
      }
      if (!this.form.email) {
        this.errors.push("Email is required.");
      }
      if (!this.form.message) {
        this.errors.push("Message is required.");
      }
      if (this.errors.length) {
        return;
      }

      // submit form
      try {
        const response = await axios.post("/api/submit-form", this.form);
        console.log("Form submitted successfully:", response);
      } catch (error) {
        console.error("Error submitting form:", error);
      }
    }
  }
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