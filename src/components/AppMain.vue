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
  <main>
    <div class="container py-5">
      <div class="row">
        <div v-for="(card, i) in store.allCards" :key="i" class="my-col-1-5 mb-4">
          <SingleCard :card="card" />
        </div>
      </div>
    </div>
  </main>
</template>

<style lang="scss" scoped>
.my-col-1-5{
  width: 20%;
}
</style>