<template>
  <form @submit.prevent="onSubmit">
    <input type="text" v-model="title">
    <button type="submit">Create</button>
  </form>
</template>


<script>
export default {
  data() {
    return {
      title: ""
    }
  },
  methods: {
    onSubmit() {
      console.log(this.title)
      if (this.title.trim()) {
        const newTodo = {
          id:Date.now(),
          title: this.title,
          completed: false
        }
        this.$emit('add-todo',newTodo)
        this.title=''

      }
    }
  }
}
</script>


<style scoped>
form {
  display: flex;
  flex-direction: row;
  justify-content: center;
  align-items: center;
  margin-bottom: 20px;
}

input {
  width: 400px;
  height: 30px;
  margin-right: 10px;
  border: 2px solid black;

}

button {
  border: none;
  padding: 10px;
  background: #2ecd2e;
  border-radius: 2px;
  color: white;
  font-size: 13px;
}

button:hover{
  background: #1fec1f;
  color: #ffffff;
  transition: all .2s linear;
}
</style>
