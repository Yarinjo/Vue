<template>
  <!-- <Header /> -->
  <div className="favorites">
    <div className="fav-title">Favourites</div>
    <div className="favorites-list">
      <FilmBlock v-for="film of film" v-bind:film="film" />
    </div>
  </div>
</template>
<script>
import FilmBlock from '/src/components/FilmBlock.vue'
export default {
  props: ['film'],
  components: {
    FilmBlock
  }
}
</script>
