<template>
  <div class="px-3">
    <ButtonsComp @new="movePosition"></ButtonsComp>

    <EscenaComp
      v-for="(item, index) in escenas"
      :key="index"
      :myEscena="item.frase"
      :class="[{ active: activeItem === index }, masClases]"
    >
    </EscenaComp>
  </div>
</template>

<script>
import axios from "axios";
import ButtonsComp from "@/components/ButtonsComp";
import EscenaComp from "@/components/EscenaComp";

export default {
  components: {
    ButtonsComp,
    EscenaComp,
  },
  data() {
    return {
      escenas: [],
      activeItem: 0,
      masClases:
        "my-4 border border-3 border-dark rounded-pill heigthCustom d-flex  justify-content-center align-items-center",
    };
  },
  methods: {
    getEscenas: function () {
      axios
        .get("/mock/dataEscena_7.json")
        .then((response) => (this.escenas = response.data))
        .catch((error) => console.log(error));
    },

    movePosition: function (option) {
      switch (option) {
        case 1:
          if (this.activeItem == 0) this.activeItem = this.escenas.length - 1;
          else this.activeItem--;
          break;
        case 2:
          if (this.activeItem === this.escenas.length - 1) this.activeItem = 0;
          else this.activeItem++;
          break;
        default:
      }
    },
    // changeMostrar: function () {
    //   console.log("changeMostrar()");
    //   this.mostrar = !this.mostrar;
    // },
  },

  mounted: function () {
    this.getEscenas();
  },
};
</script>
<style scoped>
.active {
  background-color: pink;
}
</style>
