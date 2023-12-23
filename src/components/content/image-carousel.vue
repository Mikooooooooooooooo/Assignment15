<template>
    <div>
        <div class="image__carousel">
            <img src="../../assets/left-chevron-svgrepo-com.svg" v-on:click="prevSource()" alt="" class="image__carousel-left">
            <img :src="getSource()" alt="" class="image__carousel-content">
            <img src="../../assets/right-chevron-svgrepo-com.svg" v-on:click="nextSource()" alt="" class="image__carousel-right">
        </div>
    </div>
</template> 

<script>
    export default{ 
        data() {
            return {
                index: 0 , 
            }
        } , 
        props: ['sources'] , 
        methods: { 
            getSource() { 
                return this.sources[this.index]
            } , 
            prevSource() {
                this.index-- ; 
                if (this.index == -1)
                    this.index = this.sources.length - 1 ; 
            } , 
            nextSource(){
                this.index++ ; 
                if (this.index == this.sources.length )
                    this.index = 0 ; 
            }
        }
    }
</script>

<style>

    .image__carousel{
        display: flex ; 
        position: relative ; 
        width:fit-content ; 
    }

    .image__carousel-content{
        width: 500px ; 
    }

    .image__carousel-left{
        position: absolute; 
        left: 20px ; 
        top: 48% ; 
        border-radius: 50% ; 
        transition: all .5 ease ; 
        padding: 5px;  
    }

    .image__carousel-right{ 
        position: absolute ; 
        right: 20px ; 
        top: 48% ;
        border-radius: 50% ; 
        transition: all .5 ease ; 
        padding: 5px;  
    }

    .image__carousel-left:hover{
        background: #bcc3c4; 
        opacity: .8 ; 
    }

    .image__carousel-right:hover{
        background: #bcc3c4 ; 
        opacity: .8 ; 

    }


</style>
