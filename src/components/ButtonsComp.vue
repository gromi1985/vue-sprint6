<template>
  <div class="d-flex">
    <button class="basis" @click="colorPosition(1)">Anterior</button>
    <button class="basis" @click="colorPosition(2)">Siguiente</button>
  </div>
</template>
<script>
export default {
  name: "ButtonsComp",
  methods: {
    colorPosition: function (option) {
      this.$emit("new", option);
    },
  },
};
</script>
<style scoped>
.basis {
  flex-basis: 50%;
}
</style>
