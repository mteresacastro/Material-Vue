<template>
    <h1 class="red" v-if="age < 18">Eres menor de edad</h1> 
    <h1 class="green" v-else>Eres mayor de edad</h1>
    <!-- <h1 v-show="age<18">Eres menor de edad</h1> 
        <h1 v-show="age>18">Eres mayor de edad</h1> -->
</template>

<script setup>

        let age = 18;
    
</script>

<style scoped>
.red{
    color: red;
}

.green{
    color:green
}
</style>