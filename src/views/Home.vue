<template>
  <div class="home">
    <HelloWorld msg="Jordan's Test Lab"/>
    <router-link to="/todolist">To Do List!</router-link>
  </div>
</template>

<script>
// @ is an alias to /src
import HelloWorld from '@/components/HelloWorld.vue'

export default {
  name: 'Home',
  components: {
    HelloWorld
  }
}
</script>
