<template> 
    <div>
        <div class="input__password">   

            <label class="input__password-label">{{title}}</label>

            <input type="password" v-if="hide" class="input__password-input" required>
            <input type="text" v-else class="input__password-input" required >
            

            <img class="input__password-icon" v-if="hide" @click="changeMode()" src="../../../assets/hide-svgrepo-com.svg" alt="">
            <img class="input__password-icon" v-else @click="changeMode()" src="../../../assets/show-svgrepo-com.svg" alt="">
        </div>  
    </div>
</template>

<script>
    export default{
        data() { 
            return { 
                title: 'Password' , 
                hide : true  , 
                typeInput: 'Password'
            }
        } , 
        methods: { 
            changeMode(){
                this.hide = !this.hide ; 
            }
        }
    }
</script>

<style>

    .input__password{
        width: 450px ; 
        background: #fff ; 
        padding: 20px 0 ; 
    }

    .input__password-input{ 
        height: 100% ; 
        width: 100% ; 
        outline: none ; 
        border: 2px solid ;   
        font-size: 17px ; 
        padding: 5px ;
        padding-left: 10px  ;  
        margin-top: 1vh ; 
    }

    .input__password-label{
        color: grey ; 
    }

    .input__password-icon{
        position: relative ; 
        left: 97% ; 
        bottom: 27px ; 
    }

</style>