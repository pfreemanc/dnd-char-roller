<template>
  <div id="app" class="app">
    <div v-if="!isStarted">
      <h1>DnD Character Sheet Builder</h1>
      <h2>Do you have a suggestion? Let me know!</h2>
      <button @click="onClick">Get Started</button>
    </div>
    <div v-if="isStarted">
      <Questionarre />
    </div>
  </div>
</template>

<script>
import Questionarre from "./components/Questionarre.vue";

export default {
  name: "App",
  components: {
    Questionarre,
  },
  data() {
    return {
      isStarted: false,
    };
  },
  methods: {
    onClick() {
      this.isStarted = true;
    },
  },
};
</script>

<style lang="scss">
.app {
  height: 100vh;
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
}
</style>
