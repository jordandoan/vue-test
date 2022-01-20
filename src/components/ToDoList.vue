<template>
  <div id="todo">
    <p>{{ message }}</p>

    <input v-model="newTask"><button v-on:click="addTask">Add task</button>
    <ol>
      <li v-for="todo in todos" v-bind:key="todo">
        {{ todo }}
      </li>
    </ol>

  </div>
</template>

<script>
export default {
  name: 'ToDoList',
  data () {
    return {
      newTask: "",
      message: "to do list",
      todos: [
      "Do chores",
      "Wash Dishes",
      "Do laundry",
      "Make Dinner"
      ]
    }
  },
  methods: {
    addTask () {
      this.todos.push(this.newTask)
      this.newTask = ""
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
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
