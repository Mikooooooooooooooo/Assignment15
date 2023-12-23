<template>
    <div>
        <div class="tooltip" @mouseover="show = true" @mouseout="show = false">
            <div v-if="show" class="tooltip__message">
                {{ message }}
            </div>
           <slot></slot>
        </div>  
    </div>
</template>

<script>    
    export default{
        data() {
            return { 
                show: false
            }
        } , 
        props: ['message']
    }
</script>   

<style>

    .tooltip{
        margin: 2vh  0; 
    }

    .tooltip__message{
        padding: 5px ; 
        background: gray ; 
        width: fit-content ; 
        border-radius: 5px ; 
        color: white ; 
        font-size: 14px ; 
    }

</style>
