<template>
  <div class="login-container">
    <h2>Login</h2>
    <form @submit.prevent="login" class="login-form">
      <input
        v-model="username"
        placeholder="Username"
        class="input-field"
      />
      <input
        v-model="password"
        type="password"
        placeholder="Password"
        class="input-field"
      />
      <button type="submit" class="login-button">Login</button>
    </form>
    <p v-if="error" class="error-message">{{ error }}</p>
  </div>
</template>

<script>
export default {
  data() {
    return {
      username: '',
      password: '',
      error: ''
    };
  },
  methods: {
    login() {
      if (this.username === 'JoanaParale' && this.password === 'JowanaM') {
        this.$router.push('/portfolio/profile');
      } else {
        this.error = 'Invalid login credentials';
      }
    }
  }
};
</script>

<style scoped>
/* Login container styling */
.login-container {
  max-width: 360px;
  margin: 50px auto;
  padding: 2rem;
  background-color: #f9d5d3; /* Peachy pink background */
  border-radius: 12px;
  box-shadow: 0 4px 8px rgba(0, 0, 0, 0.2);
  text-align: center;
  font-family: 'Georgia', serif; /* Updated font */
}

/* Header styling */
h2 {
  margin-bottom: 1.5rem;
  color: #4a4a4a;
  font-size: 1.8rem;
  font-weight: bold;
}

/* Login form styling */
.login-form {
  display: flex;
  flex-direction: column;
}

/* Input field styling */
.input-field {
  margin-bottom: 1rem;
  padding: 0.75rem;
  border: 1px solid #ffd1d1;
  border-radius: 6px;
  font-size: 1rem;
  color: #333;
  font-family: 'Georgia', serif; /* Updated font for input fields */
}

/* Button styling */
.login-button {
  background-color: #ff7f7f; /* Light red-pink button */
  color: white;
  border: none;
  padding: 0.75rem;
  border-radius: 6px;
  font-size: 1rem;
  font-weight: bold;
  cursor: pointer;
  transition: background-color 0.3s, transform 0.2s;
  font-family: 'Georgia', serif; /* Font applied to button */
}

.login-button:hover {
  background-color: #e76f6f;
  transform: scale(1.05);
}

/* Error message styling */
.error-message {
  color: #e74c3c;
  margin-top: 1rem;
  font-size: 0.9rem;
  font-family: 'Georgia', serif; /* Error message font */
}

/* Responsive adjustments */
@media (max-width: 480px) {
  .login-container {
    padding: 1.5rem;
  }

  h2 {
    font-size: 1.5rem;
  }
}
</style>
