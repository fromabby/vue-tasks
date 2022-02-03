<template>
    <button 
        :style="{background: color}" 
        class="btn"
        @click="onClick()"
    >{{text}}</button>
</template>

<script>
export default {
    name: 'Button',
    props: {
        text: {
            type: String,
            default: 'Button'
        },
        color: String
    },
    methods: {
        onClick() {
            let show = false
            this.$emit('toggle-add-task', !show)
        }
    }
}
</script>