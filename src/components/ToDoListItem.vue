<template>
  <li>{{ task }}</li>
</template>

<script>
export default {
  props : {
    task: String,
    index: Number
  }
} 
</script>
<style scoped>
li {
  font-size: 1.2em;
  width: 20%;
  margin: 0 auto;
}

li:hover {
  text-decoration: line-through;
}
</style>