<script>
export default {
  props: {
    film: {
      type: Object,
      required: true
    }
  }
  // data() {
  // return {
  //   id: 1,
  //   title: 'Bullet science',
  //   image: 'https://images.indianexpress.com/2022/08/bullet-train-review.jpg',
  //   year: '2022',
  //   genre: 'Action comedy',
  //   isFavorited: true
  // }
  // }
}
</script>

<template>
  <div className="film">
    <!-- <img src="{{film.image}}" alt="" /> -->
    <div className="lowerSection">
      <p className="title">{{ film.title }}</p>
      <span className="year-genre">{{ film.year }} | {{ film.genre }}</span>
    </div>

    <!-- <div className="like" onClick="{handleUnFavorite}"><img src="{Heart}" alt="like" /></div> -->
  </div>
</template>

<style>
.film {
  border: 1px solid var(--gray);
  border-radius: 20px;
  transition: all 0.2s ease-in-out;
  &:hover {
    transform: scale(1.03);
  }

  img {
    border-radius: 20px;
  }
}
.lowerSection {
  backdrop-filter: blur(20px);
  background: linear-gradient(148deg, #fff 0%, #fff 100%);
  opacity: 0.95;
  padding: 16px 20px 24px 20px;
  width: 100%;
  border-radius: 0 0 20px 20px;

  position: absolute;
  bottom: 0;

  span {
    font-weight: 400;
    font-size: 14px;
    line-height: 114%;
    color: #000;
  }
  .title {
    font-weight: 600;
    font-size: 16px;
    line-height: 150%;
    color: #000;
  }
}
.like {
  border-radius: 8px;
  padding: 8px;
  display: flex;
  position: absolute;
  top: 20px;
  right: 20px;
  backdrop-filter: blur(11.851852416992188px);
  background: linear-gradient(147deg, #fff 0%, #fff 100%);
}

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
</style>
