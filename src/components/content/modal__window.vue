<template>
    <div>
        <div class="message__box">
    
            <div @click="show = true">
                <slot></slot>
            </div>
    
            <div v-if="show" class="message__box-content" @click="show = false">
                <div class="message__box-wrapper" @click="show = true">
                    <div class="message__box-title">
                        {{ message }}
                    </div>
                </div>
            </div>
    
        </div>
    </div>
    </template>
    
    <script>
        export default{ 
            data() {
                return{
                    show: false 
                }
            } , 
            props: ['message']
        }
    </script>
    
    <style>
        .message__box-content{
            position: fixed; 
            width: 100% ; 
            height: 100vh ;  
            z-index: 2 ; 
            top: 50%;
            left: 50%;
            transform: translate(-50%, -50%);
            background-color: #fff;
            padding: 20px;
            border: 1px solid #ccc;
            box-shadow: 0 2px 5px rgba(0, 0, 0, 0.2);
            opacity: .8 ; 
    
        }
    
        .message__box-wrapper{
            position: relative ;
            width: 400px ; 
            height: 20vh;
            margin: 40vh auto 0  ; 
            background: white ; 
            border: 2px solid ; 
            padding: 20px ; 
        }
    
        .message__box-title{
            font-size: 18px ; 
        }
    
        .message__box-input{
            position: absolute ; 
            bottom: 2vh ; 
            right: 20px ;
            padding: 10px 5px ; 
            font-size: 15px ; 
            box-shadow: 0 2px 5px rgba(0, 0, 0, 0.2);
            cursor: pointer ;
        }
    
    </style>