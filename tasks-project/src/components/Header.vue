<template>
    <header>
        <h1>{{title}}</h1>
        <!-- <Button :text='!show ? "Add Task" : "Close"' :color='!show ? "green" : "blue"' @btn-click="[$emit('toggle-add-task')]"/> -->
        <Button :text='text' :color='color' @btn-click="[$emit('toggle-add-task'), toggleButton()]"/>
    </header>
</template>

<script>
import Button from './Button/Button.vue'

export default {
    name: 'Header',
    props: {
        title: {
            type: String,
            default: 'Task Tracker'
        },
        show: {
            type: Boolean,
            default: false
        }
    },
    components: {
        Button
    },
    methods: {
        toggleButton() {
            this.color = this.show ? 'green' : 'blue'
            this.text = this.show ? 'Add Task' : 'Hide'
        }
    },
    data() {
        return {
            color: 'green',
            text: 'Add Task'
        }
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