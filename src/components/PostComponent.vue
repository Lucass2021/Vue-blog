<template>
  <div>
    <div class="posts">
      <div class="post-info">
        <span>Post Id: {{ props.id }}</span>
        <div @mouseover="handleMouseOver" @mouseout="handleMouseOut" @click="handleFavorite">
            <font-awesome-icon v-show="regularHeart" class="heartIcon" :icon="['far', 'heart']" />
            <font-awesome-icon v-show="solidHeart" class="heartIcon" :icon="['fas', 'heart']" />
        </div>
      </div>
      <h2>{{ props.title }}</h2>
      <p>{{ props.text }}</p>
    </div>
  </div>
</template>

<script setup>
    import { ref, defineProps} from 'vue'
    const props = defineProps({
      id: String,
      title: String,
      text: String,
    })

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
  padding: 2rem;
  border-radius: 0.5rem;
  border: 0.125rem solid #252529;
  background: #17171A;
  margin-bottom: 2.5rem;
}

.posts:hover{
    border-radius: 0.5rem;
    border: 0.125rem solid #E07B67;
    background: #17171A;
    transition: all 0.3s ease-in-out;
}

.posts .post-info {
  display: flex;
  justify-content: space-between;
  align-items: center;
  width: 100%;
  margin-bottom: 1.25rem;
}

.posts .post-info span {
  color: #E07B67;
  font-family: Inter, monospace;
  font-size: 1rem;
  font-style: normal;
  font-weight: 500;
  line-height: normal;
}

.posts .post-info .heartIcon {
  color: #E07B67;
  width: 2rem;
  height: 2rem;
  cursor:pointer;
}

.posts h2{
  color: #FFF;
  font-family: "Space Grotesk", monospace;
  font-size: 1.5rem;
  font-weight: 500;
  margin-bottom: 0.938rem;
}

.posts p{
  color: #AFABB6;
  font-family: Inter, monospace;
  font-size: 1.25rem;
  font-weight: 500;
  line-height: 2rem;
}
</style>