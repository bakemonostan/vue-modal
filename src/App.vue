<template>
  <h1>{{ greet }}</h1>
  <div v-if="showModal">
    <Modal :header="header" :info="info" theme="sale" @close="toggleModal"
  /></div>
  <button @click="toggleModal">Show modal</button>
</template>

<script>
import Modal from './components/Modal';

export default {
  name: 'App',
  components: {
    Modal,
  },
  data() {
    return {
      greet: 'le vue',
      header: 'Tadaaaa',
      info: 'Give away ready',
      showModal: false,
    };
  },
  methods: {
    toggleModal() {
      return (this.showModal = !this.showModal);
    },
  },
};
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

h1 {
  color: red;
  font-size: 3rem;
}
</style>

