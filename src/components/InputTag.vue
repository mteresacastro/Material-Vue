<script>
 export default {
    data(){
        return{
            currentValue: '',
            tags: [],
            showErrorMessage: false,
        };
    },

    methods: {
       handleKeyDown(e){
            this.showErrorMessage = false;
            if(e.key === "Backspace" && this.currentValue === ''){
                this.tags.pop();
            }
       }, 
       handleSubmit(){
            
            if(this.currentValue!== ''){
                const exist = this.tags.some(item => item === this.currentValue);
                if (!exist){
                    this.tags.push(this.currentValue);
                    this.currentValue = "";   
                } else {
                    this.showErrorMessage = true;
                }
                
            }
        },
        deleteTag(tag){
            this.tags = this.tags.filter((item)=> item !== tag)
        }
    }
 };
</script>


<template>
    <div class="inputTag">
        <div class="tags">
            <div class="tag" v-for="(tag, index) in tags" :key= index>
            {{ tag }} <button @click="deleteTag(tag)">X</button>
            </div>
        </div>
        <form @submit.prevent="handleSubmit">
            <input type="text" v-model="currentValue" @keydown="handleKeyDown">
        </form>
        <p class="errorMessage" v-if="showErrorMessage">La etiqueta ya existe</p>
    </div>
</template>



<style scoped>

</style>
