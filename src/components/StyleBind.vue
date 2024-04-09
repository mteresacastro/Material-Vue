<template>
    <p v-bind:style="{ // se usa el camelCase al nombrar las claves. Se puede usar con guion, pero debe ir entre comillas
        backgroundColor: 'pink',
        color: c,
        border: '3px solid salmon'

    }">El mensaje se ha enviado satisfactoriamente</p>
    <button v-on:click="handleClick()"><!--v-on se acorta con @, v-bind se acorta con :.-->  Cambiar color </button> 
    </template>
    
    
    <script setup>
    import {ref} from 'vue';//si quiero que sea un valor reactivo debo aplicar una referencia
        let c = ref('black');
        const handleClick = () => {
            if(c.value === 'black'){
                c.value = 'white';
            }else{
                c.value = 'black';
            }
        };
    </script>
 
    
    <style>
 
    </style>