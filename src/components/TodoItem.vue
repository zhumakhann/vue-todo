<template>
    <li class="todo__item" v-bind:class="{'active': todo.completed}">
        <input type="checkbox" :checked="todo.completed" />
        <p>{{ todo.title }}</p>
        <button @click="$emit('del-todo', todo.id)" class='del'>X</button>
    </li>
</template>

<script>
export default {
    name: "TodoItem",
    props: ["todo"],
    methods: {
        markComplete(){
            this.todo.completed = !this.todo.completed
        }
    }
}
</script>

<style>

</style>