<script>


export default {
  data() {
    return {
      props: {
      card: Object
  }
    }
  },
  
}
</script>

<template>
  <div>
      <div>
        <img :src="card.card_image" :alt="card.name" class="w-100 ">
      </div>

      <h3>
        {{ card.name }}
      </h3>

      
     <!--  <h5>
        {{ card.species }}
      </h5> -->
    </div>
</template>

<style lang="scss" scoped>
</style>