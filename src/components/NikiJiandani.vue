<template>
  <div>{{ msg }}</div>
</template>

<script>
export default {
  name: "NikiJiandani",
  props: {
    msg: String
  }
};
</script>

<style scoped>
div {
  font-size: 2rem;
  color: aquamarine;
}
</style>