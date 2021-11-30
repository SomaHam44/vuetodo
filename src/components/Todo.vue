<template>
    <div>
        <TodoItem
         />
        <ul>
            <li 
            v-for="todo in todos"
            v-bind:key="todo.title" :title="todo.title"
            > {{todo.title}}
            <button>Edit</button></li>
            </ul>
    </div>
    
</template>
<script>
import TodoItem from './TodoItem.vue'
export default {
    props : ['todos'],
    components: {TodoItem}

}

</script>