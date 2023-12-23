<template> 
    <div>
        <div class="collapse">
            <div class="collapse__top" v-on:click="show = !show">
                <div class="collapse__title">
                    {{ title }}
                </div>
                <img v-if="!show" src="../../assets/navigation-arrow-chevron-direction-forward-move-down-icon-svgrepo-com.svg"   alt="" class="accordion__input">
                <img v-else src="../../assets/navigation-arrow-chevron-direction-forward-move-up-icon-svgrepo-com.svg" alt="" class="accordion__input">
            </div>
            <div class="collapse__text" v-if="show">
                {{ text }}
            </div>
        </div>
    </div>
</template>

<script>

    export default{ 
        data() { 
            return { 
                show: false 
            }
        },      
        props: ['title' , 'text']
    }

</script>

<style>

    .collapse{
        width: 450px ; 
        margin: 2vh 0 ; 
    }

    .collapse__top{
        display: flex ; 
        justify-content: space-between ; 
        padding: 10px ; 
        border: 2px solid ; 
        cursor: pointer ; 
    }

    .collapse__title{ 
        font-size: 18px ; 
    }

    .collapse__text{
        font-size: 17px ; 
        padding: 10px ; 
        border: 2px solid ; 
        border-top: 0 ; 
    }


</style>