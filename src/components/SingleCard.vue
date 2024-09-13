<script>


export default {
  data() {
    return {
      
    }
    
  },
  props: {
        cardName: String,
        cardImage: String,
        cardArchetype: String
  }
  
}
</script>

<template>
  <div>
      <div>
        <img :src="cardImage" :alt="cardName" class="w-100 ">
      </div>

      <h3>
        {{ cardName }}
      </h3>

      
      <h5>
        {{ cardArchetype }}
      </h5>
    </div>
</template>

<style lang="scss" scoped>
</style>