<template>
  <a href="https://google.com" target="_blank" :class="setColor" class="mb-2"
    >Google</a
  >
</template>

<script>
export default {
  props: {
    color: String,
  },
  computed: {
    setColor() {
      return this.color === "red" ? "btn btn-danger" : "btn btn-dark";
    },
  },
};
</script>

<style scoped>
a {
  width: 100%;
}
</style>
