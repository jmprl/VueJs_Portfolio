<template>
  <div class="creative-page">
    <h2>My Hobbies</h2>
    <ul class="hobby-list">
      <li v-for="(hobby, index) in hobbies" :key="index" class="hobby-item">
        <div class="hobby-info">
          <h3>{{ hobby.name }}</h3>
          <p>{{ hobby.description }}</p>
        </div>
      </li>
    </ul>
  </div>
</template>

<script>
export default {
  data() {
    return {
      hobbies: [
        {
          name: "Playing Online Games",
          description: "Games like Mobile Legends, Call of Duty, and Valorant",
        },
        {
          name: "Exploring New Experiences",
          description: "Stepping out of comfort zone and learning different things",
        },
        {
          name: "Watching Movies",
          description: "Streaming different movies and dramas",
        },
      ],
    };
  },
};
</script>

<style scoped>
/* Container styling */
.creative-page {
  max-width: 800px;
  margin: 0 auto;
  padding: 20px;
  background: linear-gradient(135deg, #ffe5d9, #ffd1c2);
  border-radius: 15px;
  box-shadow: 0 6px 12px rgba(0, 0, 0, 0.1);
  font-family: "Open Sans", sans-serif; /* Elegant body font */
  color: #4f4f4f; /* Soft, modern text color */
}

/* Heading styling */
h2 {
  text-align: center;
  margin-bottom: 30px;
  font-size: 28px;
  color: #2c3e50; /* Elegant, deep color for the heading */
  font-family: "Playfair Display", serif; /* Classy heading font */
  font-weight: 700;
}

/* Hobby list styling */
.hobby-list {
  list-style: none;
  padding: 0;
}

/* Individual hobby item styling */
.hobby-item {
  display: flex;
  align-items: flex-start;
  background-color: #ffffff;
  border: 1px solid #f0c8bb;
  border-radius: 12px;
  margin-bottom: 20px;
  padding: 20px;
  box-shadow: 0 4px 8px rgba(0, 0, 0, 0.1);
  transition: transform 0.3s ease, box-shadow 0.3s ease;
}

/* Add hover effect for hobby items */
.hobby-item:hover {
  transform: translateY(-5px);
  box-shadow: 0 8px 16px rgba(0, 0, 0, 0.15);
}

/* Hobby info styling */
.hobby-info h3 {
  margin: 0;
  font-size: 22px;
  font-family: "Playfair Display", serif; /* Classy heading font */
  color: #34495e; /* Deep gray-blue for hobby titles */
  font-weight: 600;
}

.hobby-info p {
  margin-top: 5px;
  font-size: 16px;
  font-family: "Open Sans", sans-serif; /* Body font */
  color: #7f8c8d; /* Soft gray for descriptions */
}

/* Hobby icon (if needed later) */
.hobby-icon {
  width: 50px;
  height: 50px;
  margin-right: 20px;
  border-radius: 50%;
  background-color: #ffe5d9; /* Placeholder color */
  object-fit: cover;
}
</style>
