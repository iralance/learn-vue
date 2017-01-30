<template>
    <form v-on:submit.prevent="addTodo(newTodo)">
        <div class="form-group">
            <input v-model="newTodo.title" type="text" class="form-control" placeholder="add a new title" />
        </div>
        <div class="form-group">
            <button class="btn btn-success" type="submit">add</button>
        </div>
    </form>
</template>
<style>

</style>
<script>
    export default{
        props: ['todos'],
        data(){
            return {
                newTodo:{id:null,title:'',completed:false}
            }
        },
        methods:{
            addTodo:function(newTodo){
                this.todos.push(newTodo);
                this.newTodo = {id:null,title:'',completed:false};
            },

        }
    }
</script>