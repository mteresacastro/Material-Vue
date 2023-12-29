<template>
<p v-bind:class="{ //se puede usar solo :class //v-bind asocia datos de forma unidireccional
    'danger' : hasError,
    'clase' : condicion 
}">El mensaje se ha enviado satisfactoriamente</p>
</template>


<script>
import {defineComponent} from "vue";
export default defineComponent({
    name: "ClassBind",
    setup(){
    let hasError = false; //si es true se agregaría la clase danger
        return {hasError};
    }
})
</script>

<!--//CON COMPOSITION API
<script setup> 
    let hasError = false;
</script>

//CON OPTION API
<script> 
    import {defineComponent} from "vue";
    export default defineComponent({
    name: "ClassBind",
    data(){
     return {hasError = false;} 
    }
})
</script>
-->

<style>
.danger{
    color:red;
}
</style>