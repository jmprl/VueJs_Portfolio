<template>
  <footer class="footer">
    <div class="footer-content">
      <p>&copy; 2024 Joana Parale's Portfolio. All rights reserved.</p>
      <div class="footer-social">
        <a href="https://github.com/jmprl" target="_blank" rel="noopener noreferrer" class="social-link">GitHub</a>
        <span>|</span>
        <a href="https://www.linkedin.com/in/joana-may-parale-bb243b33b?trk=contact-info" target="_blank" rel="noopener noreferrer" class="social-link">LinkedIn</a>
        <span>|</span>
        <a href="https://x.com/jwnprl" target="_blank" rel="noopener noreferrer" class="social-link">Twitter</a>
      </div>
    </div>
  </footer>
</template>

<script>
export default {
  name: 'FooTer',
};
</script>

<style scoped>
.footer {
  background-color: #f9c6d1; /* Creamy pink background */
  color: #4f4f4f; /* Soft grayish text color */
  padding: 2rem 1rem;
  text-align: center;
  width: 100%;
  margin-top: 20px;
  font-family: 'Georgia', serif; /* Elegant serif font */
  box-shadow: 0 4px 12px rgba(0, 0, 0, 0.1); /* Soft shadow for depth */
}

.footer-content {
  display: flex;
  flex-direction: column;
  align-items: center;
}

.footer-content p {
  font-size: 16px;
  margin-bottom: 1rem;
  font-weight: 500;
  color: #41142a; /* Deep maroon color */
}

.footer-social {
  margin-top: 1rem;
  display: flex;
  justify-content: center;
  gap: 1.5rem;
}

.footer-social a {
  color: #41142a; /* Maroon for links */
  text-decoration: none;
  font-size: 18px;
  font-weight: 500;
  transition: color 0.3s ease, transform 0.3s ease;
}

.footer-social a:hover {
  color: #aa366e; /* Pinkish hover color */
  transform: translateY(-3px); /* Slight lift effect */
}

.footer-social span {
  color: #41142a; /* Maroon separator */
  font-size: 20px;
}

.footer-social a:focus {
  outline: none;
  color: #aa366e;
}

@media (max-width: 768px) {
  .footer {
    padding: 1.5rem 0.5rem;
  }
  
  .footer-social {
    flex-direction: column;
    gap: 1rem;
  }
}
</style>
