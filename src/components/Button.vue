<template>
    <button @click="onClick()" :style="{background: color}" class="btn">
        {{text}}
    </button>
</template>

<script>
export default {
    name: 'HeaderButton',
    props:{
        text: String,
        color: String
    },

    methods:{
        onClick(){
           this.$emit('toggle-button')
        }
    }
}
</script>
