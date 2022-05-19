<template>
    <button @click="onClick()" :style="{background: color}" class="btn">{{text}}</button>
</template>

<script>
export default{
    name:"ToggleButton",
    props: {
        text: String,
        color: String,
    },
    methods:{
        onClick(){
            console.log("clicked")
        }
    }
}
</script>

<style scoped>
.btn{
    color: white;
    border: none;
    padding: 10px;
    cursor: pointer;
}
</style>