<script>
export default {
  props: ["data"],
  data() {
    return {};
  }
};
</script>

<template>
  <li class="list-group-item d-flex align-items-center">
    <input type="checkbox" name="" id="" v-model="data.done" >
    <div class="w-100 ml-2">
      <div class="d-flex w-100">
        <div class="card-title title w-75 mr-auto" >
          <span :class="{'done':data.done}">{{data.message}}</span>
        </div>
        <i class="far fa-star p-2"></i>
        <i class="fas fa-pencil-alt p-2"></i>
      </div>
      <div class="summary">
        <i class="far fa-calendar-alt"></i> 5/13
      </div>
    </div>
  </li>
  
</template>

<style>
.summary {
  color: #757575;
  font-size: 10px;
}

.done {
  text-decoration: line-through;
}
</style>

