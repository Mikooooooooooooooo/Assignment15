<template> 
    <div>   
        <div class="card">
            <div class="card__option">
                {{ option }}
            </div>
            <div class="card__title">
                {{ title }}
            </div>
            <div class="card__text">
                {{ text }}
            </div>
        </div>
    </div>
</template>

<script>
    export default{
        props:['option', 'title' , 'text']
    }
</script>

<style>

    .card{
        width: 300px ; 
        margin: 2vh 0 ; 
        padding: 20px ; 
        border: 2px solid ; 
    }

    .card__option{ 
        font-size: 18px ; 
    }

    .card__title{
        font-size: 22px ; 
        text-align: center ; 
        margin: 3vh 0; 
    }

    .card__text{
        font-size: 17px ; 
    }

</style>