<template>
    <div class="post" v-for="post in posts">
      <div><b>Название: </b> {{post.title}} </div>
      <div><b>Описание: </b> {{post.descr}} </div>
    </div>
</template>

<script>

export default {
    props: {
        posts: {
            type: Array,
            required: true
        }
    },
    data() {
        return {

        }
    }
}
</script>

<style>
.post {
  padding: 15px;
  border: 2px solid teal;
  margin-top: 15px;
}
</style>
