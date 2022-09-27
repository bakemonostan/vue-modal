<template>
  <div class="backdrop" @click.self="closeModal">
    <div class="modal" :class="{ sale: theme === 'sale' }">
      <h3>{{ header }}</h3>
      <p>{{ info }}</p>
    </div>
  </div>
</template>

<script>
// passing props to component
export default {
  props: ['header', 'info', 'theme'],
  methods: {
    closeModal() {
      this.$emit('close');
    },
  },
};
</script>

<!-- styling components -->
<style>
.modal {
  width: 400px;
  padding: 20px;
  margin: 100px auto;
  background: white;
  border-radius: 10px;
}

.backdrop {
  position: fixed;
  top: 0;
  background: rgba(204, 204, 204, 0.7);
  width: 100%;
  height: 100%;
}

.modal.sale {
  background: crimson;
  color: white;
}

.modal.sale.h3 {
  color: white;
}
</style>
