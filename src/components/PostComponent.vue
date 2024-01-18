<template>
    <div class="posts">
      <div class="post-info">
        <span>17 de ago, 2024</span>
        <div @mouseover="handleMouseOver" @mouseout="handleMouseOut">
            <font-awesome-icon v-show="regularHeart" class="heartIcon" :icon="['far', 'heart']" />
            <font-awesome-icon v-show="solidHeart" class="heartIcon" :icon="['fas', 'heart']" />
        </div>
      </div>
    </div>
</template>

<script setup>
    import { ref } from 'vue'

    let regularHeart = ref(true)
    let solidHeart = ref(false)

    const handleMouseOver = () => {
        regularHeart.value = false
        solidHeart.value = true
    };

    const handleMouseOut = () => {
        regularHeart.value = true
        solidHeart.value = false
    };

</script>

<style scoped>
.posts {
  display: flex;
  padding: 40px;
  border-radius: 8px;
  border: 2px solid #252529;
  background: #17171A;
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
</style>