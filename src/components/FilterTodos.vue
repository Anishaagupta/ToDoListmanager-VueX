<template>
  <div class="select-div">
   <div> <h3 class="sub-heading">All Todos</h3></div>
    <div>
      Filter Todos:
      <select @change="filterTodos($event)">
        <option value="200">200</option>
        <option value="100">100</option>
        <option value="50">50</option>
        <option value="20">20</option>
        <option value="10">10</option>
        <option value="5">5</option>
      </select>
    </div>
  </div>
</template>

<script>
import { mapActions } from "vuex";
export default {
  name: "FilterTodos",
  methods: mapActions(["filterTodos"]),
};
</script>

<style scoped>
.select-div {
  margin-top: 40px;
  display: flex;
  flex-direction: row;
  justify-content: space-between;
  width: 85%;
}
select {
  margin-top: 2rem;
  padding: 6px;
  border: #914fe5 1px solid;
}
.sub-heading{
  margin-left: 10rem;
}
</style>
