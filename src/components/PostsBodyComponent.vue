<template>
    <div class="container">
        <div class="posts-container">
            <PostComponent id="1" title="Albert" text="jotapeg"/>
        </div>
    </div>
</template>

<script setup>
import PostComponent from './PostComponent.vue';


</script>

<style scoped>
    .container{
        background: #121214;
        height: 100vh;
    }

    .posts-container{
        margin:0 auto;
        padding: 80px 0px;
        width: 1200px;
    }


    @media only screen and (max-width: 1400px) {
        .posts-container{
            width: 800px;
        }
    }

    @media only screen and (max-width: 1000px) {
        .posts-container{
            width: 600px;
        }
    }

    @media only screen and (max-width: 768px) {
        .posts-container{
            width: 500px;
        }
    }

    @media only screen and (max-width: 568px) {
        .posts-container{
            width: 300px;
        }
    }
</style>