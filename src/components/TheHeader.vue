<template>
  <header class="header">Header</header>
</template>

<script>
export default {
  beforeUnmount() {
    // Destruir as nossas libs
    // Eventos
    // Listeners
    console.log("beforeUnmount");
  },
  unmounted() {
    console.log("unmounted");
  },

  methods: {
    resize($evt) {
      console.log($evt);
    },
  },
};
</script>

<style>
.header {
  background: #000;
  color: #fff;
}
</style>
