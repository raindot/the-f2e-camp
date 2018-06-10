<script>
import InputTodo from "./InputTodo";
import Item from "./Item";

export default {
  data() {
    return {
      todos: [],
      show: false
    };
  },
  components: {
    InputTodo,
    Item
  },
  methods: {
    addTodo(text) {
      this.todos.push(text);
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
        <li class="list-group-item d-flex align-items-center">
          <input type="checkbox" name="" id="">
          <div class="w-100 ml-2">
            <div class="d-flex w-100">
              <div class="card-title title w-75 mr-auto">目前僅可新增todo</div>
              <i class="far fa-star p-2"></i>
              <i class="fas fa-pencil-alt p-2"></i>
            </div>
            <div class="summary">
              <i class="far fa-calendar-alt"></i> 5/13
            </div>
          </div>
        </li>
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
