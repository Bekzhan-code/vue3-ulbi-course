<template>
    <div>
        <h2>Список постов</h2>
        <div class="post" v-for="post in posts">
            <post-item :post="post" />
        </div>
    </div>
</template>

<script>
import PostItem from './PostItem.vue'

export default {
    components: {
        PostItem
    },
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
