<template> 
    <div>
        <div class="input__date">   
            <label class="input__date-label">{{title}}</label>
            <input type="date" class="input__date-input" required>
        </div>  
    </div>
</template>

<script>
    export default{
        data() { 
            return { 
                title: 'Date'
            }
        } , 
        methods: { 
         
        }
    }
</script>

<style>

    .input__date{
        width: 450px ; 
        background: #fff ; 
        padding: 20px 0 ; 
    }

    .input__date-input{ 
        height: 100% ; 
        width: 100% ; 
        outline: none ; 
        border: 2px solid ;   
        font-size: 17px ; 
        padding: 5px ;
        padding-left: 10px  ;  
        margin-top: 1vh ; 
    }

    .input__date-label{
        color: grey ; 
    }

</style>