<template>
  <div class="modal" v-if="active" @click.self="close">
    <div class="modal-content">
      <span class="close" @click="close">&times;</span>
      <p>Lorem Ipsum</p>
    </div>
  </div>
</template>

<script>
export default {
  props: ['active'],
  methods: {
    close() {
      this.$emit('close');
    }
  }
};
</script>

<style lang="scss" scoped>
.modal {
  align-items: center;
  justify-content: center;
  position: fixed;
  z-index: 1;
  left: 0;
  top: 0;
  width: 100%;
  height: 100%;
  overflow: auto;
  background-color: rgba(0, 0, 0, 0.4);
}

.modal-content {
  background-color: #FEFEFE;
  margin: 15% auto;
  padding: 20px;
  border: 1px solid #888888;
  width: 80%;
}

.close {
  color: #FFFFFF;
  float: right;
  font-size: 28px;
  font-weight: bold;

  &:hover, &:focus {
    color: #000000;
    text-decoration: none;
    cursor: pointer;
  }
}
</style>
