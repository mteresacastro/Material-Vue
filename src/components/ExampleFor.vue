<template>
    <ul>
        <li v-for="country in countries" v-bind:key="country.code">{{ country.name }}</li> <!--en el v-for, podriamos poner "(country, index) in countries" para usar luego como key index. v-bind de puede omitir y dejar solo :key-->
    </ul>
</template>

<script setup>
import {ref} from 'vue';
let countries= ref([
   {
    code: 'es',
    name: 'Spain'
   },
   {
    code: 'fr',
    name: 'France'
   },
   {
    code: 'it',
    name: 'Italy'
   },
   {
    code: 'pt',
    name: 'Portugal'
   } 
])
</script>

<style scoped>
</style>