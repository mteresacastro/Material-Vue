<template>
    <div class="post-card">
        <img class="post-card__img" src="../assets/que-es-un-blog.png" alt="imagen del proyecto">
        <h3>Titulo</h3>
        <p>Lorem ipsum dolor sit amet consectetur, adipisicing elit. Quas perferendis voluptatum harum maiores rem iste, ratione minus, voluptatibus distinctio nesciunt laborum facilis, sint tempore consequuntur perspiciatis tempora nisi cumque numquam?</p>
        <PostButton/>
    </div>
</template>

<script setup>
import PostButton from "./PostButton.vue";
</script>

<style scoped>
.post-card {
    width: 30%;
    padding: 1.5rem;
    margin: 1rem;
    border-radius: 15px;
    border: 1px solid rosybrown;
    text-align: center;
}
.post-card__img{
    width: 95%;
}
</style>