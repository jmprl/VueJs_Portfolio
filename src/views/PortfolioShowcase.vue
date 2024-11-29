<template>
  <div class="portfolio-showcase">
    <div class="project-card" v-for="project in projects" :key="project.id">
      <img :src="project.image" alt="Project Image" />
      <h3>{{ project.title }}</h3>
      <p>{{ project.description }}</p>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      projects: [
        {
          id: 1,
          title: "WebFit: Online System on Gym Utilization Reservation and Coach Appointment",
          description:
            "The Gym Management System aims to improve the current system by making it more efficient and effective. It includes a reliable reservation system to prevent double bookings and scheduling conflicts. The system also reduces the staff’s workload by automating tasks like booking and record tracking, which helps minimize errors and boost productivity.",
          image: require("@/assets/gym.png"),
        },
        {
          id: 2,
          title:
            "AquaTect: Innovative Design of an AI-Driven System for Crayfish Gender Detection",
          description:
            "AquaTect is an innovative system that uses IoT technology to automate the process of sorting crayfish by gender. This system helps improve efficiency in aquaculture by reducing the need for manual labor and increasing sorting accuracy. ",
          image: require("@/assets/detect.png"),
        },
      ],
    };
  },
};
</script>

<style scoped>
/* Portfolio Showcase container */
.portfolio-showcase {
  display: flex;
  flex-wrap: wrap;
  gap: 20px;
  justify-content: center;
  padding: 40px 20px;
  background-color: #f9d5d3; /* Peachy pink background */
  font-family: "Montserrat", sans-serif;
}

/* Individual project card */
.project-card {
  background-color: #fff;
  border: 1px solid #ffd1d1;
  border-radius: 12px;
  width: 300px;
  padding: 20px;
  text-align: center;
  box-shadow: 0 4px 8px rgba(0, 0, 0, 0.1);
  transition: transform 0.3s, box-shadow 0.3s;
}

.project-card:hover {
  transform: translateY(-5px);
  box-shadow: 0 6px 12px rgba(0, 0, 0, 0.15);
}

/* Project image styling */
.project-card img {
  width: 100%;
  height: 180px;
  object-fit: cover;
  border-radius: 8px;
  margin-bottom: 15px;
}

/* Project title styling */
.project-card h3 {
  font-size: 20px;
  color: #2c2c54; /* Deep blue font for titles */
  margin-bottom: 10px;
  font-weight: 700;
}

/* Project description styling */
.project-card p {
  font-size: 16px;
  color: #444444; /* Dark gray font for descriptions */
  line-height: 1.6;
}

/* Responsive adjustments */
@media (max-width: 768px) {
  .portfolio-showcase {
    padding: 20px;
  }

  .project-card {
    width: 100%;
  }
}
</style>
