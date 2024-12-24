<template>
    <form @submit.prevent>
      <h4>Создание поста</h4>
      <input type="text" placeholder="Название" v-model="title">
      <input type="text" placeholder="Описание" v-model="descr">
      <button @click="createPost">Создание</button>
    </form>
</template>

<script>
export default {
    data() {
        return {
            title: '',
            descr: ''
        }
    },
    methods: {
        createPost() {
            const newPost = {
                id: Date.now(),
                title: this.title,
                descr: this.descr,
            }
            this.$emit('create', newPost)
            this.title = '';
            this.descr = '';
        },
    }
}
</script>

<style>
form {
  display: flex;
  flex-direction: column;
}

input {
  width: 100%;
  border: 1px solid teal;
  padding: 10px 15px;
  margin-top: 15px;
}

button {
  margin-top: 15px;
  align-self: flex-end;
  padding: 10px 15px;
  background: none;
  color: teal;
  border: 1px solid teal;
}
</style>
