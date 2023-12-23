<template> 
    <div>
        <div class="form__select">
            <select class="form__select-input">          
                <option disabled selected value class="form__select-option"> {{ title }} </option>   
                <option value="" v-for="item in arr" class="form__select-option">{{ item }}</option>
            </select>
        </div>
    </div>
</template>

<script>
    export default{
        props: ['arr' , 'title' ] 
    }
</script>

<style>
    
    .form__select{
        width: 470px ; 
        background: #fff ; 
        padding: 20px 0 ; 
    }

    .form__select-input{
        width: 100% ; 
        height: 100% ; 
        padding: 5px ;
        padding-left: 10px ; 
        font-size: 17px ; 
        color: gray ; 
        outline: none ; 
        border: 2px solid black ; 
        
    }


</style>