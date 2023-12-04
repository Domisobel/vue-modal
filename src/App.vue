<template>
  <h1>{{ title }}</h1>
  <ModalWindow :header="header " :text="text" theme="sale" />
</template>

<script>
import ModalWindow from "./components/ModalWindow.vue";

export default {
  name: "App",
  components: { ModalWindow },

  data() {
    return {
      title: "First vue app",
      header: 'Sign up',
      text: 'Better faster'
    };
  },
  methods: {
    handleClick() {
      console.log(this.$refs.name);
      this.$refs.name.classList.add("active");
      this.$refs.name.focus();
    },
  },
};
</script>

<style>
#app {
  text-align: center;
}
h1 {
  display: inline-block;
  text-align: center;
  border-bottom: 1px solid violet;
  margin: 100px 600px;
}
.modal.sale {
  background: crimson;
  color: white;
}
.modal.sale h2 {
  color: white;
}
</style>
