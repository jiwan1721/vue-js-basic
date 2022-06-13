<template>
    <div>
        <h1>Todos {{id}} :{{title}}: {{completed}}</h1>
        <input type="checkbox" :value="true">
    </div>
</template>
<script>

export default {
    name:"todoItem",
    props: {
        id: {
            type: Number,
        },
        title:{
            type: String,
        },
        completed: {
            type: Boolean,
            default: true
        }
    }
}
</script>
<style scoped>

</style>