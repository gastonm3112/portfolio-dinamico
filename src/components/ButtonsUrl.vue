<template>
  <a :href="url" target="_blank" :class="setColor" class="mb-2">
    {{ title }}
  </a>
</template>

<script>
export default {
  props: {
    color: String,
    url: String,
    title: {
      type: String,
      default: "Repo Github",
    },
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
