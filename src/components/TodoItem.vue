<template>
    <li class="text">{{todo.text}}</li>
</template>

<script>
    export default {
        name: "TodoItem",
        props: ['todo'],
    }
</script>

<style scoped>
    .text {
        color: #42b983;
    }
</style>