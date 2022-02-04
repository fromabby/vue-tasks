<template>
    <footer>
        <p>Copyright</p>
        <router-link to="/about">About</router-link>
    </footer>
</template>

<script>

export default {
    name: 'Footer'
}
</script>


<style scoped>
a {
    color: gray
}

footer {
    margin-top: 30px;
    text-align: center;
}

</style>