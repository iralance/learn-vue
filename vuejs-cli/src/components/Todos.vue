<template>
    <ul class="list-group">
        <li class="list-group-item"
            v-bind:class="{'completed' : todo.completed}"
            v-for="(todo,index) in todos">{{todo.title}}
            <button class="btn btn-xs pull-right" v-bind:class="[todo.completed?'btn-success':'btn-danger']" v-on:click="toggleComplete(todo)">
                {{todo.completed?'done':'undone'}}
            </button>
            <button class="btn btn-warning btn-xs pull-right" v-on:click="deleteTodo(todo)">Del</button>
        </li>
    </ul>
</template>
<style>
    .completed{color:green;text-decoration: line-through;}
</style>
<script>
    export default{
        props: ['todos'],

        methods:{
            deleteTodo:function(todo){
                this.todos.splice(index,1);
            },
            toggleComplete:function(todo){
                todo.completed = !todo.completed;
            }
        }
    }
</script>