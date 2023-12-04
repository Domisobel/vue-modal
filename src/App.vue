<template>
  <h1>{{ title }}</h1>
  <p>Welcome...</p>
  <div v-if="showModal">
    <ModalWindow :header="header" :text="text" theme="sale" @close="toggleModal"/> 
  </div>
  <button @click="toggleModal">Open modal</button>
</template>

<script>
import ModalWindow from "./components/ModalWindow.vue";

export default {
  name: "App",
  components: { ModalWindow },

  data() {
    return {
      title: "First vue app",
      header: "Sign up",
      text: "Better faster",
      showModal: false
    };
  },
  methods: {
    toggleModal() {
      this.showModal = !this.showModal
    }
  }
};
</script>

<style>
#app {
  text-align: center;
  margin: 120px auto;
}

.modal.sale {
  background: crimson;
  color: white;
}
.modal.sale h2 {
  color: white;
}
</style>
