<template> 
    <div>
        <div class="form__textarea">   
            <label class="form__textarea-label">{{title}}</label>
            <textarea class="form__textarea-input" required></textarea>
        </div>  
    </div>
</template>

<script>
    export default{
        data() { 
            return { 
                title: 'Enter Your text'
            }
        } , 
        methods: { 
         
        }
    }
</script>

<style>

    .form__textarea{
        width: 450px ; 
        background: #fff ; 
        padding: 20px 0 ; 
    }

    .form__textarea-input{ 
        height: 100% ; 
        width: 100% ; 
        outline: none ; 
        border: 2px solid ;   
        font-size: 17px ; 
        padding: 5px ;
        padding-left: 10px  ;  
        margin-top: 1vh ; 
    }

    .form__textarea-label{
        color: grey ; 
    }

</style>