<template>
  <div class="profile-page">
    <div class="profile-image">
      <img :src="photo" alt="Profile Picture" />
    </div>
    <div class="profile-details">
      <h2>{{ name }}</h2>
      <p>{{ bio }}</p>
      <div class="social-links">
        <a :href="social.facebook" target="_blank" rel="noopener">
          <i class="fab fa-facebook"></i>
        </a>
        <a :href="social.linkedin" target="_blank" rel="noopener">
          <i class="fab fa-linkedin"></i>
        </a>
        <a :href="social.github" target="_blank" rel="noopener">
          <i class="fab fa-github"></i>
        </a>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      name: "Joana May B. Parale",
      bio: "A Computer Engineering graduate from the Technological Institute of the Philippines, driven by a passion for innovation and problem-solving, with expertise in hardware design, software development, and IoT systems. Dedicated to lifelong learning and excellence, with a strong commitment to advancing technology and making meaningful contributions to the engineering field.",
      photo: require("@/assets/pic.jpeg"),
      social: {
        facebook: "https://www.facebook.com/share/SUc88B4aZYZ7ZJ5e/?mibextid=LQQJ4d",
        linkedin: "https://www.linkedin.com/in/joana-may-parale-bb243b33b?trk=contact-info",
        github: "https://github.com/jmprl",
      },
    };
  },
};
</script>

<style scoped>
/* Overall profile container */
.profile-page {
  text-align: center;
  padding: 40px 20px;
  background-color: #f9d5d3; /* Peachy pink background */
  font-family: "Montserrat", sans-serif;
  color: #4a4a4a;
  border-radius: 15px;
  max-width: 800px;
  margin: 40px auto;
  box-shadow: 0 4px 12px rgba(0, 0, 0, 0.1);
}

/* Profile image styling */
.profile-image img {
  width: 180px;
  height: 180px;
  border-radius: 50%;
  object-fit: cover;
  border: 4px solid #ff8a9c; /* Soft pink border */
  margin-bottom: 20px;
}

/* Profile name styling */
.profile-details h2 {
  font-size: 28px;
  font-weight: 700;
  color: #333;
  margin-bottom: 15px;
  font-family: "Playfair Display", serif;
}

/* Profile bio styling */
.profile-details p {
  font-size: 16px;
  color: #555;
  margin-bottom: 30px;
  line-height: 1.6;
  max-width: 600px;
  margin: 0 auto;
}

/* Social links styling */
.social-links a {
  display: inline-block;
  margin: 0 15px;
  color: #ff6670; /* Soft pink for icons */
  font-size: 28px;
  transition: color 0.3s, transform 0.3s;
}

.social-links a:hover {
  color: #b23a48; /* Darker pink on hover */
  transform: scale(1.2);
}

/* Responsive adjustments */
@media (max-width: 768px) {
  .profile-page {
    padding: 20px;
  }

  .profile-details h2 {
    font-size: 24px;
  }

  .profile-details p {
    font-size: 14px;
  }

  .social-links a {
    font-size: 24px;
  }
}
</style>
