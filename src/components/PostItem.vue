<template>
    <div class="post-item">
        <div>
            <div><b>Название: </b> {{post.title}} </div>
            <div><b>Описание: </b> {{post.descr}} </div>
        </div>
        <my-button>Удалить</my-button>
    </div>
</template>

<script>
export default {
    props: {
        post: {
            type: Object,
            required: true
        }
    }
}
</script>

<style scoped>
.post-item {
    display: flex;
    justify-content: space-between;
}
</style>