<template> 
    <div>
        <div class="buttons__dropdawn">
            <button type="button" @click="show = !show" class="buttons__dropdawn-input">
                {{ title }}
            </button> 
            <a v-if="show" class="buttons__dropdawn-link" v-for="(link , index) in links" :href="link">link {{ index  }}</a>
        </div>
    </div>
</template>

<script>
    export default { 
        data() { 
            return { 
                show: false 
            }
        } ,
        props: ['title' , 'links']
    }
</script>

<style>
    
    .buttons__dropdawn-input{       
       width: 160px ; 
       padding: 10px ; 
       text-align: center ; 
       margin: 20px 10px ; 
       margin-left: 0 ; 
       font-weight: bold ; 
       border: 2px solid gray;
       background: transparent ; 
       color: gray;
       cursor: pointer ; 
       overflow: hidden ;    
       font-family: sans-serif ; 
       text-transform: uppercase ;     
       margin-bottom: 0px ;   
    }

    .buttons__dropdawn-link{
        display: block ; 
        text-decoration: none ;
        color: gray ; 
        width: 136px ; 
        padding: 10px ; 
        border-left: 2px solid ; 
        border-right: 2px solid ; 
    }

    .buttons__dropdawn-link:last-of-type{
        border-bottom: 2px solid ; 
    }


</style>