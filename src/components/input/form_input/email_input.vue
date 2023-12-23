<template> 
    <div>
        <div class="input__email">   
            <label class="input__email-label">{{ title }}</label>
            <input type="email" class="input__email-input" required>
        </div>  
    </div>
</template>

<script>
    export default{
        data() { 
            return { 
                title: 'Email'
            }
        } , 
    }
</script>

<style>

    .input__email{
        width: 450px ; 
        background: #fff ; 
        padding: 20px 0 ; 
    }

    .input__email-input{ 
        height: 100% ; 
        width: 100% ; 
        outline: none ; 
        border: 2px solid ;   
        font-size: 17px ; 
        padding: 5px ;
        padding-left: 10px  ;  
        margin-top: 1vh ; 
    }

    .input__email-label{
        color: grey ; 
    }

</style>