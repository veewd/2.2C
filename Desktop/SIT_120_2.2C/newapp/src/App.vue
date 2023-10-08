<template>
  <div id="app">
    <!-- Sidebar Navigation Menu -->
    <nav class="sidebar">
      <ul>
        <li><a @click="scrollToSection('welcome')">Welcome</a></li>
        <li><a @click="scrollToSection('html')">HTML</a></li>
        <li><a @click="scrollToSection('css')">CSS</a></li>
        <li><a @click="scrollToSection('javascript')">JavaScript</a></li>
        <li><a @click="scrollToSection('vue')">Vue 3</a></li>
      </ul>
    </nav>

    <!-- Main Content - HelloWorld Component -->
    <HelloWorld msg="Welcome to Your Vue.js App" />

    <!-- The rest of your HelloWorld component content goes here -->
  </div>
</template>

<script>
import HelloWorld from './components/HelloWorld.vue';

export default {
  name: 'App',
  components: {
    HelloWorld
  },
  methods: {
    scrollToSection(sectionId) {
      const element = document.getElementById(sectionId);
      if (element) {
        element.scrollIntoView({ behavior: 'smooth' });
      }
    }
  }
};
</script>

<style>
/* Global Styles */
body {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}

/* Sidebar Styles */
.sidebar {
  position: fixed;
  top: 0;
  left: 0;
  width: 200px;
  height: 100%;
  background-color: #333;
  color: #fff;
  overflow-y: auto;
}

.sidebar ul {
  list-style-type: none;
  padding: 0;
}

.sidebar li {
  margin: 10px 0;
}

.sidebar a {
  color: #fff;
  text-decoration: none;
  display: block;
  padding: 10px;
  transition: background-color 0.3s ease;
}

.sidebar a:hover {
  background-color: #42b983;
}
</style>
