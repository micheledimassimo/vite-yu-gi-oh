<script>
export default {
  data() {
    return { 
      message: 'Yu\-Gi\-Oh API',
      logoImg: 'https://upload.wikimedia.org/wikipedia/commons/1/11/Yu-Gi-Oh%21_%28Logo%29.jpg'
    }
  }
}
</script>

<template>
  <header class="d-flex">
    <img :src="logoImg"
    alt="Yu Gi Oh">
    <h1>
      {{ message }}
    </h1>
  </header>
</template>

<style lang="scss" scoped>
@use '../assets/scss/partials/variables' as *;

header {
 

  padding: 20px;
  img {
    width: 80px;
  }
}

h1 {
  font-size: 3rem;
}
</style>
