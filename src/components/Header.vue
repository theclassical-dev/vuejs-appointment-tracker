<template>
    <header>
        <h1>{{ title }}</h1>
        <Button @btn-click="$emit('toggle-add-task')" 
        :text="showAddTasks ? 'Close' : 'Add Appoinment'" 
        :color="showAddTasks ? 'red' : 'green'" />
    </header>
</template>

<script>
import Button from './Button'

    export default {
        name: 'Header',
        props: {
            title: String,
            showAddTasks: Boolean
        },
        components: {
            Button
        }
    }
</script>

<style scoped>
    header {
        display: flex;
        justify-content: space-between;
        align-items: center;
        margin-bottom: 20px;
    }
</style>