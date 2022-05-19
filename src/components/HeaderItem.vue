<template>
<header>
    <h1>Todo Tracker</h1>
    <ToggleButton text="Add Task" color="green"/>
</header>
</template>

<script>
import ToggleButton from './ToggleButton.vue'

export default{
    name:"HeaderItem",
    components: {
        ToggleButton
    }
}
</script>

<style scoped>
header{
    display: flex;
    align-items: center;
    justify-content: space-between;
}
</style>