<template>
    <h3>{{counter}}</h3>
    <button @click="addCounter">Incrementar</button>
</template>

<script> //si usamos setup aqui, no haria falta el export, ni name, ni setup(), ni return.
import { defineComponent, ref } from 'vue';
export default defineComponent({
    name: 'CounterComposition',
    setup(){//setup no es reactivo, necesita ref, para permanecer atento a los cambios de esos datos)
        let counter = ref(0);
        const addCounter = () => {
            counter.value++ // EL VALUE PORQUE ES UN OBJETO DE REFERENCIA
        }
        return {counter, addCounter}
    }

})
</script>

<style>
</style>