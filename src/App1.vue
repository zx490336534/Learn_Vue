<template>
    <div id="app">
        {{message}}
        <ol>
            <todo-item v-for="item in groceryList" v-bind:todo="item" v-bind:key="item.id"></todo-item>
        </ol>
    </div>
</template>

<script>
    import TodoItem from './components/TodoItem.vue'

    export default {
        name: "app",
        data() {
            return {
                message: 'Hello Vue',
                groceryList: [{id: 0, text: "蔬菜"}, {id: 1, text: "奶酪"}]
            }
        },
        components: {
            TodoItem
        }
    }
</script>

<style scoped>

</style>