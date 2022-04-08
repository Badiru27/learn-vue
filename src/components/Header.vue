<template>
    <header>
        <h1>
            {{title}}
        </h1>
        <HeaderButton @toggle-button="$emit('show-add-task' )" :text="showAddTask?'Cancel': 'Add Task'" :color="showAddTask? 'red':'green'"/>
        <!-- <HeaderButton text="Update Task" color="blue" /> -->
    </header>

</template>

<script>
import HeaderButton from './Button.vue'

export default{
    name: 'HomeHeader',
    props:{
        title: String,
        showAddTask: Boolean
    },
    components: {
        HeaderButton
    }

}
</script>

<style scoped>
header{
    display: flex;
    justify-content: space-between;
    align-items: center;
    margin-bottom: 20px;
}
</style>

 