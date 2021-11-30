<template>
    <div>
        <TodoItem
         />
        <ul>
            <li 
            v-for="todo in todos"
            v-bind:key="todo.title" :title="todo.title"
            @todo-item-changed="Changed"
            > {{todo.title}}
            <button>Edit</button></li>
            </ul>
    </div>
    
</template>
<script>
import TodoItem from './TodoItem.vue'
export default {
    props : ['todos'],
    components: {TodoItem},
    methods: {
        Changed(e) {
            this.$emit('todo-item-changed', e)

        }
    }

}

</script>