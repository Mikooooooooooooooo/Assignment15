<template> 
    <div>
        <div class="input__group">
            <span class="input__group-icon">{{ title }}</span>
            <input type="text" class="input__group-input">
        </div>
    </div>
</template>

<script>

    import Text_Input from './form_input/text_input.vue'

    export default {
        components: {
            'text-input' : Text_Input
        } , 
        props: ['title']
    }
</script>

<style>

    .input__group-input{ 
        position: relative ; 
        left: -5px ; 
        height: 100% ; 
        width: 380px  ; 
        outline: none ; 
        border: 2px solid ;   
        font-size: 17px ; 
        padding: 5px ;
        padding-left: 10px  ;  
        margin-top: 1vh ; 
        margin-left: 0; 
    }

    .input__group-icon{
        height: 100% ; 
        padding: 5.6px  ; 
        font-size: 17px ; 
        margin: 0 ; 
        border: 2px solid ; 
        border-right: 0 ; 
    }

</style>