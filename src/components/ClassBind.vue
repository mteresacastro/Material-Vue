<template>
<p v-bind:class="{ //se puede usar solo :class
    'danger' : hasError,
    'clase' : condicion 
}">El mensaje se ha enviado satisfactoriamente</p>
</template>


<script>
import {defineComponent} from "vue";
export default defineComponent({
    name: "ClassBind",
    setup(){
        let hasError = false;
        return {hasError};
    }
})
    


</script>


<style>
.danger{
    color:red;
}
</style>