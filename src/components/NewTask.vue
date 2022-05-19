<template>
    <input type="text"/>
    <button class="btn">Submit</button>
</template>

<script>
import ToggleButton from './ToggleButton.vue'

    export default{
        name: "NewTask",
        components: ToggleButton,
        methods: {
            onClick(){}
        }
    }
</script>
