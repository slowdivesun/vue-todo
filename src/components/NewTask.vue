<template>
    <form @submit="(e)=>onSubmit(e)">
        <input @change="(e)=>onChange(e)" type="text"/>
        <button class="btn">Submit</button>
    </form>
</template>

<script>
import ToggleButton from './ToggleButton.vue'

    export default{
        name: "NewTask",
        components: ToggleButton,
        data(){
            return {
                newTask: "",
                status: false,
            }
        },
        methods: {
            onSubmit(e){
                e.preventDefault();
                var tasks = JSON.parse(localStorage.getItem("tasks"));
                tasks.push({task: this.newTask, status: this.status});
                localStorage.setItem("tasks", JSON.stringify(tasks))
                console.log(JSON.parse(localStorage.getItem("tasks")))
            },
            onChange(e){
                this.newTask = e.target.value
            }
        }
    }
</script>
