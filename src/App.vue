<template>
  <h1>{{ title }}</h1>
  <ModalWindow/>
</template>

<script>
import ModalWindow from './components/ModalWindow.vue'

export default {
  name: 'App',
  components: { ModalWindow },
  data() {
    return {
      title: 'First vue app'
      }
    },
    methods: {
      handleClick() {
        console.log(this.$refs.name)
        this.$refs.name.classList.add('active')
        this.$refs.name.focus()
    }
  }
}


</script>

<style scoped>
h1 {
  
  display: flex;
  justify-content: center;
  border-bottom: 1px solid violet;
  margin:  100px 600px;
}

</style>
