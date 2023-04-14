<template>
  <div>
    <TheHeader v-if="showHeader" />
    <h1>Hello World</h1>
    <br />
    <input v-model="name" type="text" />
    {{ name }} <br />

    <button @click="showHeader = !showHeader">Ativar e desativar header</button>
  </div>
</template>

<script>
import TheHeader from "@/components/TheHeader";
export default {
  name: "App",
  components: { TheHeader },
  data() {
    return {
      name: "Jon Snow",
      showHeader: true,
    };
  },
  // CRIAÇÃO
  // Preparar o componente
  // Ajax, inicializar algumas variáveis
  // Não tem acesso ao template (DOM)

  // MONTAGEM
  // Inicializar um lib externa (new Lib())
  // Precisa de acesso ao template (DOM)
  // Tem acesso ao template (DOM)

  // ATUALIZAÇÃO
  // Debug
  // Update

  // DESMONTAGEM
  // Remover tudo o que for necessário (lib->destroy())
  // para liberar memória

  // HOOKS
  beforeCreate() {
    console.log("beforeCreate");
    console.log("Estado:", this.name);
    console.log("DOM:", this.$el);
  },
  created() {
    console.log("created");
    console.log("Estado:", this.name);
    console.log("DOM:", this.$el);
  },
  beforeMount() {
    console.log("beforeMount");
    console.log("Estado:", this.name);
    console.log("DOM:", this.$el);
  },
  mounted() {
    console.log("mounted");
    console.log("Estado:", this.name);
    console.log("DOM:", this.$el);
  },
  beforeUpdate() {
    console.log("beforeUpdate", this.name);
  },
  updated() {
    console.log("updated", this.name);
  },

  watch: {},

  computed: {},

  methods: {},
};
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  color: #2c3e50;
  margin: 60px;
}
</style>
