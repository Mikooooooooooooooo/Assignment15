<template> 
    <div>
        <div class="input__text">   
            <label class="input__text-label">{{title}}</label>
            <input type="text" class="input__text-input" required>
        </div>  
    </div>
</template>

<script>
    export default{
       props: ['title']
    }
</script>

<style>

    .input__text{
        width: 450px ; 
        background: #fff ; 
        padding: 20px 0 ; 
    }

    .input__text-input{ 
        height: 100% ; 
        width: 100% ; 
        outline: none ; 
        border: 2px solid ;   
        font-size: 17px ; 
        padding: 5px ;
        padding-left: 10px  ;  
        margin-top: 1vh ; 
    }

    .input__text-label{
        color: grey ; 
    }

</style>