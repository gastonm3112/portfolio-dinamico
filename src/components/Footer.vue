<template>
  <footer id="footer" class="mt-3">
    <p class="p-4 mb-0 footer_desc">&copy; Gastón Martinez - {{ year }}</p>
  </footer>
</template>

<script>
export default {
  computed: {
    year() {
      return new Date().getFullYear();
    },
  },
};
</script>

<style scoped>
#footer {
  background: #000;
  color: #fff;
  text-align: center;
}
.footer_desc {
  font-size: 1.4em;
}
</style>
