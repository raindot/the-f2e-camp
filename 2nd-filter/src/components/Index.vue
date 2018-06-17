<script>
import SideFilter from "./SideFilter.vue";
import Contents from "./Contents.vue";

export default {
  components: {
    SideFilter,
    Contents,
  },
};
</script>

<template>
  <div>
    <nav class="navbar navbar-dark bg-primary">
      <a class="navbar-brand" href="#">HaveFun</a>
        <form class="form-inline my-2 my-lg-0">
        <input class="form-control mr-sm-2" type="search" placeholder="Search" aria-label="Search">
    </form>
    </nav>
    <div class="d-flex">
      <side-filter></side-filter>
      <contents></contents>
    </div>
    
  </div>
</template>

<style>
</style>
