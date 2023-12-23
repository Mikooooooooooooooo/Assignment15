<template> 
    <div>
        <label for="input__file-input" class="input__file">
            <div class="input__file-title">
                {{ title }}
            </div>
        </label>
        <input id="input__file-input" type="file"/>
    </div>
</template>

<script>

    export default{ 
        props: ['title']
    }

</script>

<style>

    #input__file-input{
        display: none;
    }

    .input__file{
        border: 1px solid #ccc;
        display: inline-block;
        padding: 6px 12px;
        cursor: pointer;
        line-height: 30px ; 
        width: 160px; 
        text-align: center ; 
        background: #fff ; 
        border: 2px solid ;
    }


    .input__file-title{
        display: inline ;
        position: relative; 
        right: 11px ;  
        width: 20px; 
        transition: all .3s ease ; 

    }



</style>