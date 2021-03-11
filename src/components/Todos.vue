<template>
    <div>
        <h2 class="title">Todo List</h2>
        <ul v-bind:key="todo.id" class="todo__list" v-for="todo in todos">
            <!-- <h3>{{todo.name}}</h3> -->
            <TodoItem v-bind:todo="todo" v-on:del-todo="$emit('del-todo', todo.id)"/>
        </ul>
    </div>
</template>
<script>

import TodoItem from './TodoItem'

export default {
    name: "Todos",
    props: ["todos"],
    components: {
        TodoItem,
    }
}
</script>

<style scoped>

</style>