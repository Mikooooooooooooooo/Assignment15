<template>
    <div>   
        <div class="pagination">
            <img src="../../assets/left-chevron-svgrepo-com.svg"  @click="previous()" alt="" class="pagination__left">
            <div class="pagination__number">
                {{ page }}
            </div>
            <img src="../../assets/right-chevron-svgrepo-com.svg" @click="next()" alt="" class="pagination__right">
        </div>
    </div>
</template>

<script>

    export default{
        props: ['current' , 'max'] , 
        data () { 
            return{
                page: this.current , 
                isLeft: false 
            }
        } , 
        methods: {
            previous() {
                this.page-- ; 
                if (this.page == 0)
                    this.page = this.max
            } , 
            next() {
                this.page++ ; 
                if (this.page - 1 == this.max  )
                    this.page = 0  
            }
        }
    }

</script>


<style>

    .pagination{
        display: flex ; 
    }

    .pagination__number{
        font-size: 22px ; 
        padding: 2px 6px ; 
        background: #e6e6e6; 
        margin: 0 5px ; 
    }

    .pagination__left{
        padding: 2px ; 
        background: #e6e6e6; 
        transition: all .3 ease ; 
    }

    .pagination__left:hover{
        background: #d1d4cf;
        cursor: pointer ;
    }

    .pagination__right{
        padding: 2px ;
        background: #e6e6e6; 
        transition: all .3 ease ; 
    }

    .pagination__right:hover{
        background: #d1d4cf;
        cursor: pointer ;
    }


</style>