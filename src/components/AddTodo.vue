<template>
    <div class="add-todo-form">
        <form @submit="addTodo">
            <input type="text" v-model="title" name="title" placeholder="Add Tooo ...">
            <input type="submit" name="submit" value="Submit" class="btn">
        </form>
    </div>
</template>

<script>
//import { uuid } from 'vue-uuid';
export default {
    name:"AddTodo",
    data(){
        return {
            title:""
        }
    },
    methods:{
       addTodo(e) {
           e.preventDefault();
           const newTodo = {
               //id: uuid.v4(),
               title: this.title,
               completed:false
           }

           //Send todo up

           this.$emit("new-todo", newTodo);
           this.title ="";
       }
    }
}
</script>

<style scoped>
.add-todo-form{
    margin-top: 88px;
    padding: 5px;
}
    form{
        display: flex;
        margin-top: 12px;
    }

    input[type="text"]{
        flex:10;
        padding: 5px;
    }

    input[type="submit"]{
        flex:2;
    }
    .btn{
        margin-left: 8px;
    }


</style>

