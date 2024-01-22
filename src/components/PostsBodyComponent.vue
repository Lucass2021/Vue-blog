<template>
    <div class="container">
        <div class="posts-container">
            <PostComponent 
                v-for="post in postData" :key="post.id"
                :id="post.id" 
                :title="post.title" 
                :text="post.body"
            />
        </div>
    </div>
</template>

<script setup>
import PostComponent from './PostComponent.vue';
import { ref, onMounted } from "vue"

let postData = ref([])

const handlePostApiRequest = async () => {
    const request = await fetch(`https://jsonplaceholder.typicode.com/posts`)
    const json = await request.json()
    postData.value = json
}

onMounted(() => {
    try {
        console.log("Running API")
        handlePostApiRequest()
    } catch (error) {
        console.log("API error", error)
    }
})
</script>

<style scoped>
    .container{
        background: #121214;
        height: 100%;
    }

    .posts-container{
        margin:0 auto;
        padding: 5rem 0rem;
        width: 75rem;
    }


    @media only screen and (max-width: 1400px) {
        .posts-container{
            width: 50rem;
        }
    }

    @media only screen and (max-width: 1000px) {
        .posts-container{
            width: 37.5rem;
        }
    }

    @media only screen and (max-width: 768px) {
        .posts-container{
            width: 31.25rem;
        }
    }

    @media only screen and (max-width: 568px) {
        .posts-container{
            width: 18.75rem;
        }
    }
</style>