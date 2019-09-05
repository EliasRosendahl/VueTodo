<template>
    <div>
        <h1>
            Test
        </h1>
       
        <Todo text="test"></Todo>
        <Todo 
              v-for="todo in todos"
              v-bind:key= todo.id
              v-bind:title= todo.text
              ></Todo>
    </div>
</template>

<script>
    import Todo from './Todo.vue'
    export default {
        name: "TodoList",
        components: {
            Todo
        },
        data: function () {
            return {
                todos: [
                    { id: 1, text: "Task 1" },
                    { id: 2, text: "Task 2" }
                ]
            }
        }
    }
</script>

<style></style>