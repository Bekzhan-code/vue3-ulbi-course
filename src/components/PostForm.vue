<template>
    <form @submit.prevent>
      <h4>Создание поста</h4>
      <my-input type="text" placeholder="Название" v-model="title" />
      <my-input type="text" placeholder="Описание" v-model="descr" />
      <my-button class="submit-btn" @click="createPost">Создание</my-button>
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

<style scoped>
form {
  display: flex;
  flex-direction: column;
}

.submit-btn {
  margin-top: 15px;
  align-self: flex-end;
}
</style>
