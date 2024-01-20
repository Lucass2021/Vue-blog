<template>
  <div>
    <div class="posts">
      <div class="post-info">
        <span>Aug 17, 2024</span>
        <div @mouseover="handleMouseOver" @mouseout="handleMouseOut" @click="handleFavorite">
            <font-awesome-icon v-show="regularHeart" class="heartIcon" :icon="['far', 'heart']" />
            <font-awesome-icon v-show="solidHeart" class="heartIcon" :icon="['fas', 'heart']" />
        </div>
      </div>
      <h2>What is programming language? Get to know the main ones.</h2>
      <p>One of the most popular branches of information technology, the programming field continues to have a high demand for work precisely due to the speed at which technological devices are advancing.</p>
    </div>

    <div class="posts">
      <div class="post-info">
        <span>Aug 17, 2024</span>
        <div @mouseover="handleMouseOver" @mouseout="handleMouseOut" @click="handleFavorite">
            <font-awesome-icon v-show="regularHeart" class="heartIcon" :icon="['far', 'heart']" />
            <font-awesome-icon v-show="solidHeart" class="heartIcon" :icon="['fas', 'heart']" />
        </div>
      </div>
      <h2>What is programming language? Get to know the main ones.</h2>
      <p>One of the most popular branches of information technology, the programming field continues to have a high demand for work precisely due to the speed at which technological devices are advancing.</p>
    </div>
  </div>
</template>

<script setup>
    import { ref } from 'vue'

    let regularHeart = ref(true)
    let solidHeart = ref(false)
    let clickedFavorite = ref(false)

    const handleMouseOver = () => {
        regularHeart.value = false
        solidHeart.value = true
    };

    const handleMouseOut = () => {
        if(clickedFavorite.value === false){
          regularHeart.value = true
          solidHeart.value = false
        }
    };

    const handleFavorite = () => {
        clickedFavorite.value = !clickedFavorite.value
        regularHeart.value = !regularHeart.value
        solidHeart.value = !solidHeart.value
    }

</script>

<style scoped>
.posts {
  display: flex;
  flex-direction: column;
  padding: 40px;
  border-radius: 8px;
  border: 2px solid #252529;
  background: #17171A;
  margin-bottom: 40px;
}

.posts:hover{
    border-radius: 8px;
    border: 2px solid #E07B67;
    background: #17171A;
    transition: all 0.3s ease-in-out;
}

.posts .post-info {
  display: flex;
  justify-content: space-between;
  align-items: center;
  width: 100%;
  margin-bottom: 20px;
}

.posts .post-info span {
  color: #E07B67;
  font-family: Inter, monospace;
  font-size: 16px;
  font-style: normal;
  font-weight: 500;
  line-height: normal;
}

.posts .post-info .heartIcon {
  color: #E07B67;
  width: 32px;
  height: 32px;
  cursor:pointer;
}

.posts h2{
  color: #FFF;
  font-family: "Space Grotesk", monospace;
  font-size: 24px;
  font-weight: 500;
  margin-bottom: 15px;
}

.posts p{
  color: #AFABB6;
  font-family: Inter, monospace;
  font-size: 20px;
  font-weight: 500;
  line-height: 32px
}
</style>