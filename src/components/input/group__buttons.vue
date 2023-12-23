<template> 
    <div>
        <div class="group__buttons">
            <button type="button" v-for="item in buttons" class="group__buttons-input">
                {{ item }}
            </button>
        </div>
    </div>
</template>

<script>
    export default { 
        props: ['buttons']
    }
</script>

<style>
    
    .group__buttons-input{       
       width: fit-content ; 
       padding: 10px 20px ; 
       text-align: center ; 
       margin: 20px 0 ; 
       font-weight: bold ; 
       border: 2px solid gray;
       background: transparent ; 
       color: gray;
       cursor: pointer ; 
       overflow: hidden ;    
       font-family: sans-serif ; 
       text-transform: uppercase ;       
    }

    .group__buttons-input:not(:last-of-type){
        border-right: 0 ; 
    }


</style>