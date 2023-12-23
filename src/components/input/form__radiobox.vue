<template> 
    <div>
        <div class="form__radiobox">
            <div class="form__radiobox-title">
                    {{ title }}
            </div>
            <div class="form__radiobox-box" v-for="(item , index) in items">
                <input type="radio" :id="item + index" :name="title"   class="form__checkbox-input">
                
                <label :for="item + index" class="form__radiobox-label">{{ item }}</label>
            </div>
        </div>
    </div>
</template>

<script>

    export default{
        data() { 
            return { 

            }
        } , 
        props: ['title' , 'items']
    }

</script>

<style>
    
    .form__radiobox{
        width: 450px ; 
        background: #fff ; 
        padding: 20px 0 ; 
    }

    .form__radiobox-title{
        font-size: 17px ; 
        font-family: 'Poppins' , sans-serif ; 
        font-weight: 600 ; 
        margin-bottom: 1.5vh ; 
    }

    .form__radiobox-label{
        position: relative ; 
        bottom: 3px ; 
        margin-left: 10px ; 
        color: #4c4c4c ; 
        font-family: 'Poppins' , sans-serif ; 
        font-weight: 600 ; 
        font-size :15px ; 
        cursor: pointer ; 
    }

    .form__radiobox-box{
        margin-bottom: .5vh ; 
    }

    .form__radiobox-input{
        width: 17px ; 
        height: 17px ; 
        border: 2px gray solid ; 
        cursor: pointer ;
        accent-color: gray ; 
    }

</style>