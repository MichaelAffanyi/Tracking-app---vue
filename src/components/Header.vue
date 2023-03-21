<template>
    <header>
        <h1>{{title}}</h1>
        <Button 
            @btn-click="$emit('btn-click')" 
            :text="showAddTask ? 'close' : 'Add Task'" 
            :color="showAddTask ? 'red' : 'green'"
        />
    </header>
</template>

<script>
import Button from './Button.vue';
export default {
    name: 'Header',
    props: {
        title: String,
        showAddTask: Boolean
    },
    components: {
        Button
    },
    emits: ['btn-click']
}
</script>

<style scoped>
    header {
        display: flex;
        justify-content: center;
        align-items: center;
        margin-bottom: 20px;
    }
</style>