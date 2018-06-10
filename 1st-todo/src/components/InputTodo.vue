<script>
export default {
  data() {
    return {
      text: ""
    };
  },
  methods: {
    addItem() {
      this.$emit("addTodo", this.text);
      this.text = "";
    },
    cancelInput() {
      this.$emit("cancelInput");
    }
  }
};
</script>

<template>
  <div class="input-box">
    <div class="input-group border-bottom">
      <div class="input-group-prepend">
        <div class="input-group-text">
          <input type="checkbox" aria-label="Checkbox for following text input">
        </div>
      </div>
      <input type="text" v-model="text" class="form-control todo-input" placeholder="Type something here..." aria-label="Text input with checkbox">
      <div class="input-group-append">
        <span class="input-group-text">
          <i class="far fa-star"></i>
          <i class="fas fa-pencil-alt"></i>
        </span>
      </div>
    </div>
    <div class="card-body todo-body">
      <div class="d-flex mx-auto">
        <i class="far fa-calendar-alt"></i>
        <div class="todo-detail">
          <h5 class="card-title title">Deadline</h5>
          <input class="input-time" type="text" placeholder="yy/mm/dd">
          <input class="input-time" type="text" placeholder="hh:mm">
        </div>
      </div>
      <div class="d-flex">
        <i class="far fa-file"></i>
        <div class="todo-detail">
          <h5 class="card-title title">File</h5>
          <div class="add-file-btn">+</div>
        </div>
      </div>
      <div class="d-flex">
        <i class="far fa-comment-dots"></i>
        <div class="todo-detail">
          <h5 class="card-title title">Comment</h5>
          <textarea class="comment" name="" id="" cols="30" rows="3"></textarea>
        </div>
      </div>
    </div>
    <div class="">
      <button class="btn btn-outline-secondary cancel-input" @click="cancelInput">⨯ Cancel</button>
      <button class="btn btn-primary" @click="addItem">+ Add Task</button>
    </div>


  </div>

</template>

<style>
* {
  box-sizing: border-box;
}

.input-group-text {
  border: none;
  border-radius: 0;
  background-color: #f2f2f2;
}

.todo-input {
  background-color: #f2f2f2;
  border: none;
}
.todo-body {
  padding-left: 78px;
  padding-right: 78px;
  background-color: #f2f2f2;
}

.todo-detail {
  padding-left: 9px;
  padding-bottom: 25px;
}

.title {
  font-size: 20px;
}

.input-time {
  width: 162px;
  height: 35px;
  border: none;
  padding: 8px 16px;
}

.add-file-btn {
  width: 32px;
  height: 32px;
  text-align: center;
  line-height: 32px;
  color: white;
  cursor: pointer;
  background-color: #c8c8c8;
}

.comment {
  width: 445px;
}

.btn {
  width: 49.5%;
  border-radius: 0%;
  border: none;
}

.cancel-input {
  color: #d0021b;
}
</style>
