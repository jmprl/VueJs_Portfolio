<template>
  <div class="contact-page">
    <h2>Contact Me</h2>
    <form @submit.prevent="submitForm" class="contact-form">
      <input
        v-model="form.name"
        placeholder="Name"
        required
        class="form-input"
      />
      <input
        v-model="form.email"
        type="email"
        placeholder="Email"
        required
        class="form-input"
      />
      <textarea
        v-model="form.message"
        placeholder="Message"
        required
        class="form-textarea"
      ></textarea>
      <button type="submit" class="form-button">Send Message</button>
    </form>
    <p v-if="submitted" class="thank-you-message">
      Thanks for reaching out! I'll get back to you soon.
    </p>
  </div>
</template>

<script>
export default {
  data() {
    return {
      form: {
        name: '',
        email: '',
        message: ''
      },
      submitted: false
    };
  },
  methods: {
    submitForm() {
      if (this.form.name && this.form.email && this.form.message) {
        // Simulate form submission
        this.submitted = true;
        console.log('Form Submitted', this.form);
        // Clear form after submission
        this.form = { name: '', email: '', message: '' };
      }
    }
  }
};
</script>

<style scoped>
.contact-page {
  max-width: 600px;
  margin: 0 auto;
  padding: 20px;
  text-align: center;
  background-color: #ffd8cc; /* Pinkish peach background */
  border-radius: 10px;
  box-shadow: 0 4px 8px rgba(0, 0, 0, 0.1);
  font-family: 'Georgia', serif; /* Elegant font */
}

h2 {
  font-size: 28px;
  color: #6b3a2a; /* Darker pinkish peach for contrast */
  margin-bottom: 20px;
  font-weight: bold;
}

.contact-form {
  display: flex;
  flex-direction: column;
}

.form-input,
.form-textarea {
  width: 100%;
  padding: 10px;
  margin: 10px 0;
  border-radius: 5px;
  border: 1px solid #e6a89e;
  font-size: 16px;
  font-family: 'Georgia', serif; /* Matching elegant font */
}

.form-textarea {
  height: 120px;
  resize: vertical;
}

.form-button {
  padding: 12px 20px;
  margin-top: 10px;
  background-color: #e6a89e; /* Subtle peach shade */
  border: none;
  border-radius: 5px;
  color: white;
  font-size: 16px;
  cursor: pointer;
  font-family: 'Georgia', serif;
  transition: background-color 0.3s ease, transform 0.2s ease;
}

.form-button:hover {
  background-color: #d4948c; /* Slightly darker peach on hover */
  transform: scale(1.05); /* Slight zoom effect */
}

.thank-you-message {
  margin-top: 20px;
  color: #6b3a2a; /* Matching h2 color */
  font-size: 18px;
  font-family: 'Georgia', serif;
  font-style: italic;
}
</style>
