<script setup>
import { RouterLink, RouterView } from 'vue-router'
import FilmBlock from './components/FilmBlock.vue'
import FilmList from './components/FilmList.vue'
</script>

<script>
export default {
  name: 'app',
  data() {
    return {
      film: [
        { id: 1, title: 'Bullet', favourited: true, year: '2022', genre: 'Sci-fi' },
        { id: 2, title: 'House', favourited: true, year: '2022', genre: 'Sci-fi' },
        { id: 3, title: 'France', favourited: false, year: '2022', genre: 'Sci-fi' }
      ]
    }
  }
}
</script>

<template>
  <header>
    <nav>
      <RouterLink to="/"> Home</RouterLink>
      <RouterLink to="/about">About</RouterLink>
    </nav>
  </header>
  <FilmList v-bind:film="film" />

  <RouterView />
</template>

<style>
.favorites-list {
  display: grid;
  grid-template-columns: 1fr 1fr 1fr;
  gap: 25px;
}
.favorites {
  padding: 0 42px 0 32px;

  img {
    object-fit: cover;
    width: 100%;
    height: 100%;
  }
}
.fav-title {
  font-weight: 600;
  font-size: 20px;
  color: var(--white);

  margin-bottom: 24px;
}

body {
  font-family: 'Poppins', sans-serif;
  background: grey;
  color: var(--white);
}
html,
body {
  height: 100%;
}

.container {
  display: grid;
  grid-template-columns: auto 1fr;
  height: 100%;
}
#root {
  height: 100%;
}
</style>
