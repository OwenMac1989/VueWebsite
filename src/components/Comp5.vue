<template>
  <footer class="container-fluid py-4 bg-danger-subtle">
    <p class="text-center">
      Landscapes 24487 Carlee Circles, Suite 536, Raphaelleton, Missippi 24562 |
      Established 2000<br />
      Contact us by phone <a href="tel:+1208-200-1736">+1(208)-200-1736</a> or
      email <a href="mailto:care@landscapes.com">care@landscapes.com</a>
    </p>
  </footer>
</template>

<script>
export default {
  name: 'Comp5',
  props: {
    msg: String,
  },
};
</script>

<style scoped>
body{
  background-color: #e8eddf;
}
div {
  background-color: #e8eddf;
}
h3 {
  margin: 40px 0 0;
}
ul {
  list-style-type: none;
  padding: 0;
}
li {
  display: inline-block;
  margin: 0 10px;
}
a {
  color: #42b983;
}
</style>
