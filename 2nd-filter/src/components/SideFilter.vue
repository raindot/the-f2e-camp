<script>
export default {};
</script>

<template>
  <div class="side-filter">
    <form action="">
      <div class="form-group">
        <label for="">Location</label>
        <select name="" id="">
          <option value="Taiwan">Taiwan</option>
        </select>
      </div>
      <div class="form-group">
        <h5>Date</h5>
        <div>
          <label for="">From</label>
          <input type="date">
        </div>
        <div>
          <label for="">To</label>
          <input type="date">
        </div>
      </div>
      <div class="form-group">
        <div class="form-check">
          <input class="form-check-input" type="checkbox" value="" id="all">
          <label class="form-check-label" for="all">All</label>
        </div>
        <div class="form-check">
          <input class="form-check-input" type="checkbox" value="" id="entertainment">
          <label class="form-check-label" for="entertainment">Entertainment</label>
        </div>
      </div>
    </form>
  </div>
</template>

<style>
.side-filter {
  background-color: #EBEBEB;
  min-height: 100vh;
}
</style>
