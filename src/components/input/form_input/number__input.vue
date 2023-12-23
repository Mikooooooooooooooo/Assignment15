<template> 
    <div>
        <div class="input__number">   
            <label class="input__number-label">{{title}}</label>
            <input type="number" class="input__number-input" required>
        </div>  
    </div>
</template>

<script>
    export default{
        data() { 
            return { 
                title: 'Number'
            }
        } , 
        methods: { 
         
        }
    }
</script>

<style>

    .input__number{
        width: 450px ; 
        background: #fff ; 
        padding: 20px 0 ; 
    }

    .input__number-input{ 
        height: 100% ; 
        width: 100% ; 
        outline: none ; 
        border: 2px solid ;   
        font-size: 17px ; 
        padding: 5px ;
        padding-left: 10px  ;  
        margin-top: 1vh ; 
    }

    .input__number-label{
        color: grey ; 
    }

</style>