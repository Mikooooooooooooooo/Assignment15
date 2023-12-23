<template>
    <div>
        <div class="badges">
            <a :href="link" class="badges__link"> {{ title }}</a>
            <div class="badges__count">{{ count }}</div>
        </div>
    </div>
</template>

<script>
    
    export default{ 
        props: ['title' , 'count' , 'link']
    }

</script>

<style>
    .badges{
        display: flex ;
        margin: 1vh 0 ; 
    }

    .badges__link{
        font-size: 25px ; 
    }

    .badges__count{
        width: 20px ; 
        height: 20px ; 
        background: gray ; 
        color: white ; 
        text-align: center ; 
        line-height: 20px ; 
        border-radius: 50% ; 
    }

</style>