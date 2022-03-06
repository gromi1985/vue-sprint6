<template>
  <div
    id="mainElement"
    class="d-flex flex-column justify-content-center align-items-center container"
  >
    <div class="d-flex flex-column justify-content-start screen">
      <h1 class="text-center">Bienvenido al tutorial de consejos</h1>
      <p>
        Lorem ipsum dolor sit amet consectetur adipisicing elit. Voluptate,
        ipsa! Rerum maiores necessitatibus saepe quo! Ut in natus quia obcaecati
        unde atque itaque commodi minus! Ut fugiat maiores suscipit atque?
        Dignissimos provident itaque sed quasi ducimus aut nobis aspernatur,
        tempore nulla voluptatibus maxime quae nostrum consectetur impedit
        molestiae, laboriosam ipsum!
      </p>

      <p>Lorem ipsum dolor sit amet consecte</p>
    </div>
    <div class="d-flex justify-content-end screen">
      <router-link to="Home">
        <button>Iniciar</button>
      </router-link>
    </div>
  </div>
</template>

<script>
export default {
  name: "ScreenView",
  methods: {
    initScreen: function () {
      console.log("initScreen");
      this.$emit("initNew");
    },
  },
};
</script>

<style scoped>
#mainElement {
  height: 100vh;
}
.screen {
  width: 100%;
  /* padding-right: 50px;
  padding-left: 50px; */
}
.iniTutorial {
  flex-basis: 30%;
}

button {
  width: 100px;
}

p {
  font-size: 1.3rem;
}
</style>
