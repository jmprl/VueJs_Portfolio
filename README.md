# VueJs_Portfolio
This portfolio app is designed to showcase my skills, projects, and achievements. Developed using **Vue.js**, it includes various pages such as a Profile page, Portfolio Showcase, Contact page, and Creative page, each offering a unique insight into my work and creative side. The app also includes a login page for authentication (this feature can be expanded with further backend integration).

## Features
- **Login Page**: Allows users to authenticate (authentication logic can be implemented).
- **Profile Page**: Contains personal information, education, and skills.
- **Portfolio Showcase**: A collection of projects, with details and links to live demos or repositories.
- **Contact Page**: A form for users to contact me.
- **Creative Page**: Displays my hobbies, creative projects, and side work.

## Technologies Used
- **Vue.js**: JavaScript framework used for building the application.
- **Vue Router**: For routing between pages.
- **CSS**: Custom styles to make the app visually appealing and responsive.
- **Axios**: To send HTTP requests, such as submitting the contact form.

## How to Run Locally

### Prerequisites
Make sure you have the following installed:
- Node.js (You can download it from [here](https://nodejs.org/))
- npm or yarn (to manage dependencies)

### Steps to Run:
1. Clone the repository:
   ```bash
   git clone https://github.com/portfolio.git
   ```

2. Navigate to the project directory:
   ```bash
   cd portfolio
   ```

3. Install dependencies:
   ```bash
   npm install
   ```

4. Start the development server:
   ```bash
   npm run serve
   ```

5. Open your browser and go to `http://localhost:8080` to view the application.

## Contribution
Feel free to fork this repository and make contributions via pull requests. Any feedback or suggestions are welcome.

## License
This project is open-source and available under the MIT License. See the [LICENSE](LICENSE) file for more details.
```

### Code Structure with Comments

Here’s an example of how to structure your code with comments:

```javascript
<template>
  <!-- Main section for Profile page -->
  <div class="profile-page">
    <h1>{{ userName }}</h1> <!-- Display the user's name -->
    <p>{{ userBio }}</p>    <!-- Display the user's bio -->
  </div>
</template>

<script>
export default {
  name: "ProfilePage",
  data() {
    return {
      // User's name to be displayed in the profile
      userName: "Joana Parale",
      
      // Short description of the user
      userBio: "A passionate developer with expertise in frontend technologies, focusing on user-centric design and development."
    };
  }
};
</script>

<style scoped>
/* Style for profile page container */
.profile-page {
  text-align: center;
  padding: 20px;
}

/* Style for the header (name) */
h1 {
  font-size: 32px;
  color: #333;
}

/* Style for the bio text */
p {
  font-size: 18px;
  color: #555;
}
</style>
```

### Key Sections to Comment:

1. **Template Section**:
   - Comment where you define the layout of your page.
   - Explain the role of each element, especially if they have dynamic content (like `{{ userName }}`).

2. **Script Section**:
   - Comment on the `data()` function, describing the variables and their purpose (e.g., `userName` holds the name of the user).
   - Briefly describe any methods, computed properties, or lifecycle hooks used in the component.

3. **Style Section**:
   - Comment on the specific styles and explain their purpose (e.g., `h1` style changes the font size and color of the user’s name).
   - If using complex CSS (like grid, flexbox, or custom properties), include comments to clarify their purpose.
