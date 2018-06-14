<script>
import InputTodo from "./InputTodo";
import Item from "./Item";

export default {
  data() {
    return {
      todos: [{ message: "測試資料" }],
      show: false
    };
  },
  components: {
    InputTodo,
    Item
  },
  methods: {
    addTodo(text) {
      let todo = {};
      todo.message = text;
      todo.done = false;
      this.todos.push(todo);
      this.show = false;
    }
  }
};
</script>

<template>
  <div class="mycontainer mx-auto">

    <nav class="navbar navbar-dark bg-primary">
      <ul class="navbar-nav nav-todo w-100">
        <li class="nav-item">
          <a href="" class="nav-link">My Tasks</a>
        </li>
        <li class="nav-item">
          <a href="" class="nav-link">In Progress</a>
        </li>
        <li class="nav-item">
          <a href="" class="nav-link">Completed</a>
        </li>
      </ul>
    </nav>
    <div class="card" style="width: 620px;">
      <input-todo @addTodo="addTodo" @cancelInput="show = false" v-if="show === true">
      </input-todo>
      <div class="card-header add-task-btn" @click="show = true" v-else>+ Add Task</div>

      <ul class="list-group list-group-flush">
        
        <item v-for="(todo, idx) in todos" :key="idx" :data="todo"></item>
      </ul>
    </div>
  </div>

</template>

<style>
* {
  box-sizing: border-box;
  margin: 0;
  padding: 0;
}

.mycontainer {
  width: 620px;
  margin: 0 auto;
}

.nav-todo {
  justify-content: space-around;
  flex-direction: row;
}

.add-task-btn {
  cursor: pointer;
}

.summary {
  color: #757575;
  font-size: 10px;
}
</style>
