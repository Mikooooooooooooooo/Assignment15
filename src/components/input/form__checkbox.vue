<template> 
    <div>
        <div class="form__checkbox">
            <div class="form__checkbox-title">
                    {{ title }}
            </div>
            <div class="form__checkbox-box" v-for="item in items">
                <input type="checkbox" :id="item"  class="form__checkbox-input">
                <label :for="item" class="form__checkbox-label">{{ item }}</label>
            </div>
        </div>
    </div>
</template>

<script>

    export default{
        props: ['title' , 'items']
    }

</script>

<style>
    
    .form__checkbox{
        width: 450px ; 
        background: #fff ; 
        padding: 20px 0 ; 
    }

    .form__checkbox-title{
        font-size: 17px ; 
        font-family: 'Poppins' , sans-serif ; 
        font-weight: 600 ; 
        margin-bottom: 1.5vh ; 
    }

    .form__checkbox-label{
        position: relative ; 
        bottom: 3px ; 
        margin-left: 10px ; 
        color: #4c4c4c ; 
        font-family: 'Poppins' , sans-serif ; 
        font-weight: 600 ; 
        font-size :15px ; 
        cursor: pointer ; 
    }

    .form__checkbox-box{
        margin-bottom: .5vh ; 
    }

    .form__checkbox-input{
        width: 17px ; 
        height: 17px ; 
        border: 2px gray solid ; 
        cursor: pointer ;
        accent-color: gray ; 
    }

</style>