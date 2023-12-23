<template>
    <div>
        <div class="silders">
            <input type="range" class="sliders__input" :min="min" :max="max" :value="value">
        </div>
    </div>
</template>

<script>

    export default{
        props:['min' , 'max' , 'value']
    }

</script>

<style>

    .sliders__input{ 
        accent-color: gray ; 
    }

</style>    