<template>
  <nav>
    <div id="buttonInit" class="mb-5 text-center bg-secondary">
      <router-link to="/">Inicio</router-link>
    </div>
    <router-view></router-view>
  </nav>
</template>

<script>
export default {
  data() {
    return {
      mostrarHomeView: false,
    };
  },
};
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  /* text-align: center; */
  color: #2c3e50;
}

nav {
  padding: 30px;
}

nav a {
  font-weight: bold;
  color: #2c3e50;
}

nav a.router-link-exact-active {
  /* color: #42b983; */
  display: none;
}
#buttonInit {
  width: 100px;
}
#buttonInit > a {
  font-size: 20px;
  color: white;
}
</style>
