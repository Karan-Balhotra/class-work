<script setup>
import { RouterLink, RouterView } from 'vue-router'
import HelloWorld from './components/HelloWorld.vue'
</script>

<template>
  <div>
    <header class="header-bar">
      <div class="logo">Karan Balhotra</div>
      <nav>
        <RouterLink to="/about">Resume</RouterLink>
        <RouterLink to="/project" style="color: white;">Contact me form</RouterLink>
      </nav>
    </header>
    
    <main>
      <RouterView />
    </main>
  </div>
</template>

<style scoped>
.header-bar {
  display: flex;
  align-items: center;
  justify-content: space-between;
  padding: 1rem;
  background-color:black;
  box-shadow: 0px 2px 4px rgba(0, 0, 0, 0.1);
}

.logo {
  font-size: 1.5rem;
  font-weight: bold;
  color: white;
}

nav {
  display: flex;
  gap: 1.5rem;
  font-size: 1rem;
}

nav a.router-link-active {
  color: white;
  font-weight: bold;

}

nav a {
  text-decoration: none;
  color: #666;
  transition: color 0.3s ease;
}

nav a:hover {
  color: #333;
}

main {
  padding: 2rem;
}

@media (max-width: 768px) {
  .header-bar {
    flex-direction: column;
    align-items: flex-start;
  }

  nav {
    margin-top: 1rem;
  }

  .logo {
    margin-bottom: 1rem;
  }
}
</style>
