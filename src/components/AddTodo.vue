<template>
  <div>
    <h3 class="heading">Todo List Manager In Vue And VueX</h3>
    <div class="add">
      <form @submit="onSubmit">
        <input type="text" v-model="title" placeholder="Add Todo...">
        <input type="submit" value="Submit">
      </form>
    </div>
  </div>
</template>

<script>
import { mapActions } from "vuex";
export default {
  name: "AddTodo",
  data() {
    return {
      title: ""
    };
  },
  methods: {
    ...mapActions(["addTodo"]),
    onSubmit(e) {
      e.preventDefault();
      this.addTodo(this.title);
      this.title=""
    }
  }
};
</script>

<style scoped>
form {
  display: flex;
  width: 70%;
}
.heading{
  text-align: center;  
}

.add{
  display: flex;
  justify-content: center;
}
input[type="text"] {
  flex: 10;
  padding: 10px;
  border: 1px solid #914FE5;
  border-radius: 5px;
  outline: 0;
}

input[type="submit"] {
  flex: 2;
  margin-left: 20px;
  background:  #914FE5;
  color: #fff;
  border: 1px #914FE5 solid;
  border-radius: 5px;
  cursor: pointer;
  font-size: 18px ;
}
</style>
