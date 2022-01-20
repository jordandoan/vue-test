<template>
  <div id="todo">
    <h2>{{ message }}</h2>

    <input v-model="newTask" v-on:keyup.enter="addTask"><button @click="addTask">Add task</button>
    <div>
      <ul>
        <ListItem 
          v-for="(todo, index) in todos"
          :task=todo
          v-bind:key="index" 
          @click="removeTask(index)"
        />
      </ul>
    </div>
  </div>
</template>

<script>
import ListItem from '@/components/ToDoListItem.vue'
export default {
  name: 'ToDoList',
  components: {ListItem},
  data () {
    return {
      newTask: "",
      message: "to do list",
      todos: [
        "Do chores",
        "Wash Dishes",
        "Do laundry",
        "Make Dinner"
      ],
    }
  },
  methods: {
    addTask () {
      if (this.newTask.trim()) {
        this.todos.push(this.newTask)
        this.newTask = ""
      } else {
        alert("please type something in the box")
      }
    },
    removeTask (i) {
      this.todos.splice(i, 1)
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
h3 {
  margin: 40px 0 0;
}

a {
  color: #42b983;
}
</style>
