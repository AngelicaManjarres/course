<template>
<div>
  <div v-show="showModal">
    <Modal theme="sale" @close="toggleModal">
      <h1>This is the title</h1>
      <p>This is the content of the card</p>
    </Modal>
  </div>
  <button @click="toggleModal">Show Modal</button>
</div>
  
</template>

<script>
import Modal from './components/Modal.vue'

export default {
  name: 'App',
  components: {
    Modal
  },
  data() {
    return {
      header: "Prop down to child",
      text: "This is content passed prop",
      showModal: false
    }
  },
  methods: {
    toggleModal() {
      this.showModal = !this.showModal
    }
  }
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
