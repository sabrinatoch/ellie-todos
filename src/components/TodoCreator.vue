<script setup>
    import { ref, reactive } from "vue";
    import TodoButton from "./TodoButton.vue";

    const emit = defineEmits(['create-todo']);

    const todoState = reactive({
        todo: "",
        invalid: null,
        errMsg: ""
    });

    const createTodo = () => {
        todoState.invalid = null;
        if (todoState.todo !== "") {
            emit('create-todo', todoState.todo);
            todoState.todo = "";
            return;
        } // if
        todoState.invalid = true;
        todoState.errMsg = "Todo value cannot be empty";
    };

</script>

<template>
    <div class="input-wrap" :class="{ 'input-err' : todoState.invalid }">
        <input type="text" v-model="todoState.todo"/>
        <TodoButton @click="createTodo()"/>
    </div>
    <p v-show="todoState.invalid" class="err-msg">{{  todoState.errMsg }}</p>
</template>