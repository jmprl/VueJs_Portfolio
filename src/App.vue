<template>
  <div id="app">
    <!-- Navigation Bar -->
    <NavBar />

    <!-- Main Content Area where pages will be rendered -->
    <main>
      <transition name="fade" mode="out-in">
        <router-view></router-view> <!-- Vue Router renders the active component here -->
      </transition>
    </main>

    <!-- Footer -->
    <FooTer />
  </div>
</template>

<script>
import NavBar from './components/NavBar.vue';
import FooTer from './components/FooTer.vue';

export default {
  name: 'App',
  components: {
    NavBar,
    FooTer
  }
};
</script>

<style>
#app {
  font-family: 'Arial', sans-serif;
  color: #2c3e50;
  display: flex;
  flex-direction: column;
  min-height: 100vh;
}

main {
  flex: 1;
  padding: 20px;
}

footer {
  background-color: #333;
  color: white;
  padding: 1rem;
  text-align: center;
  width: 100%;
  margin-top: auto;
}
</style>
