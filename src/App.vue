<template>
  <div class="app">
    <post-form @create="createPost"/>
    <post-list :posts="posts"/>
  </div>
</template>

<script>
import PostList from './components/PostList.vue';
import PostForm from './components/PostForm.vue';

export default {
  components: {
    PostList, PostForm
  },
  data() {
    return {
      posts: [
        {id: 1, title: "JavaScript", descr: "Описание поста"},
        {id: 2, title: "JavaScript 2", descr: "Описание поста 2"},
        {id: 3, title: "JavaScript 3", descr: "Описание поста 3"},
      ],
    }
  },
  methods: {
    createPost(post) {
      this.posts.push(post)
    }
  }
}
</script>

<style>
* {
  margin: 0;
  padding: 0;
}

.app {
  padding: 20px;
}
</style>