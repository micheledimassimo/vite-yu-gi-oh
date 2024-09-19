<script>
import SingleCard from './SingleCard.vue';
import { store } from '../store.js';

export default {
  data() {
    return {
      store
    }
  },
  components: {
    SingleCard

  }
}
</script>

<template>
  
    <div class="container py-5">
      <div class="">
        <div>
          <input type="text" placeholder="Search Card">
          <select >
            <option value="">Select Archetype</option>
          </select>
        </div>
        <div class="row" >
          <SingleCard class="my-col-1-5 mb-4" v-for="(card, index) in store.allCards" :key="index" :cardName="card.name" :cardImage="card.card_images[0].image_url" :cardArchetype="card.archetype" />
        </div>
      </div>
    </div>
  
</template>

<style lang="scss" scoped>
.my-col-1-5{
  width: 20%;
}
</style>