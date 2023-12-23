<template> 
    <div>
        <div class="buttons__button">
            <button type="button" class="buttons__button-input">
                {{ title }}
            </button>
        </div>
    </div>
</template>

<script>
    export default { 
        props: ['title']
    }
</script>

<style>
    
    .buttons__button-input{       
       width: 100px ; 
       padding: 10px ; 
       text-align: center ; 
       margin: 20px 10px ; 
       margin-left: 0 ; 
       font-weight: bold ; 
       border: 2px solid gray;
       background: transparent ; 
       color: gray;
       cursor: pointer ; 
       overflow: hidden ;    
       font-family: sans-serif ; 
       text-transform: uppercase ;       
    }


</style>