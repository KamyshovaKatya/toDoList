<template>
    <ul>
        <li v-for="(todo, index) in todos" v-on:click="deleteTodo(index)" v-bind:key="index">{{ todo }}</li>
    </ul>
</template>

<script>
export default {
    props: ['todos'],
    methods: {
        deleteTodo(index){
            this.$emit('delete-todo', index);
        }
    }
}
</script>
<style>
    ul {
        margin: 0;
        padding: 0;
        list-style: none;
    }

    li {
        display: block;
        border: 2px solid #008cf0;
        margin: 10px 0;
        padding: 10px 20px;
        cursor: pointer;
    }

    li:hover {
        background: #e0ffff;
    }
</style>