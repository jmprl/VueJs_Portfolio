<template>
  <nav class="navbar">
    <!-- Logo -->
    <div class="navbar-logo">
      <h1>My Portfolio</h1>
    </div>

    <!-- Navigation Links -->
    <ul class="navbar-links">
      <li>
        <router-link to="/portfolio/profile">Profile</router-link>
      </li>
      <li>
        <router-link to="/portfolio/showcase">Showcase</router-link>
      </li>
      <li>
        <router-link to="/portfolio/contact">Contact</router-link>
      </li>
      <li>
        <router-link to="/portfolio/creative">Creative</router-link>
      </li>
      <li>
        <router-link to="/login">Logout</router-link>
      </li>
    </ul>
  </nav>
</template>

<script>
export default {
  name: "NavBar",
};
</script>

<style scoped>
/* Navbar styling */
.navbar {
  background-color: #f9c6d1; /* Soft creamy pink */
  padding: 1rem;
  display: flex;
  justify-content: space-between;
  align-items: center;
  color: white;
  font-family: 'Georgia', serif; /* Set font to Georgia for the navbar */
}

/* Logo styling */
.navbar-logo h1 {
  margin: 0;
  font-size: 24px;
  font-family: 'Georgia', serif; /* Georgia font for the logo */
  color: #e91e63; /* Darker pink for the logo text */
}

/* Navbar links container */
.navbar-links {
  list-style: none;
  display: flex;
  gap: 1.5rem;
  margin: 0;
  padding: 0;
}

/* Individual link styling */
.navbar-links li {
  display: inline;
}

.navbar-links a {
  color: #41142a; /* Creamy white for links */
  text-decoration: none;
  font-size: 18px;
  font-weight: 500;
  transition: color 0.3s ease;
}

/* Hover effect for links */
.navbar-links a:hover {
  color: #ff7f7f; /* Light coral pink for hover effect */
}
</style>
