<template> 
    <div>
        <div class="forms">
            <form action="/submit_form" method="post">
                <text-input v-for="item in items" :title="item"></text-input>
                <email-input ></email-input>
                <form-textarea></form-textarea>
                <input type="submit" class="forms__input" value="Submit">
            </form>
        </div>
    </div>
</template>

<script>

import Text_Input from './form_input/text_input.vue'
import Button_Buttons from './buttons/buttons-button.vue'
import Email_Input from './form_input/email_input.vue'
import Form_Textarea from './form__textarea.vue'
    export default{
        props: ['items'] , 
        components: { 
            'text-input' : Text_Input , 
            'button-buttons' : Button_Buttons , 
            'email-input' : Email_Input , 
            'form-textarea' : Form_Textarea 
        }
    }
</script>

<style>
    .forms__input{
       width: 100px ; 
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
    }
</style>