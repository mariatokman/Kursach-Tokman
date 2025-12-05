<template>
  <section class="about-page">
    <div class="about-card">
      <h1 class="page-title">Наша история в розовом цвете</h1>
      <div class="about-text">
        <p>
          Розовый — это не просто цвет. Это заявление. Это сила, мягкость и уверенность в одном флаконе.
          Наш магазин родился из желания перезагрузить восприятие этого удивительного оттенка и вернуть
          ему былую славу, но уже на новых условиях.
        </p>

        <p>
          Здесь вы не найдете банальных решений. Мы предлагаем дерзкий, современный и порой
          неожиданный взгляд на розовую палитру. Наша философия — это смелость быть разной. От нежных
          пастельных тонов до ультра-ярких фуксий — каждая вещь в нашем ассортименте призвана подчеркнуть
          вашу уникальность.
        </p>

        <p>Мы создаем тренды, а не следуем за ними.</p>

        <p>С любовью к смелым решениям, РО</p>
      </div>
    </div>

    <section class="popular">
      <h2>Популярное сейчас</h2>
      <div class="popular__grid">
        <div class="popular-card" v-for="item in items" :key="item.name">
          <div class="popular-card__image">
            <img :src="item.image" :alt="item.name" />
          </div>
          <div class="popular-card__content">
            <div class="popular-card__price-row">
              <span class="price">{{ item.price }} ₽</span>
              <span class="brand">{{ item.brand }}</span>
            </div>
            <p class="popular-card__name">{{ item.name }}</p>
            <p class="popular-card__rating">★ {{ item.rating }} отзывов</p>
          </div>
          <router-link :to="item.link" class="popular-card__btn">Подробнее</router-link>
        </div>
      </div>
    </section>
  </section>
</template>

<script setup>
const items = [
  {
    name: 'Розовые спортивные штаны',
    price: '5000',
    brand: 'LOOK AT NE',
    rating: '4.9 (79)',
    image: '/assets/Images/Pants5.png',
    link: '/product/pants',
  },
  {
    name: 'Лодочки розового цвета',
    price: '3000',
    brand: 'Rosso Como',
    rating: '4.8 (77)',
    image: '/assets/Images/Shoes6.png',
    link: '/product/shoes',
  },
  {
    name: 'Свитшот осенний',
    price: '2000',
    brand: 'Пальмира',
    rating: '4.7 (34)',
    image: '/assets/Images/Shirt5.png',
    link: '/product/sweatshirt',
  },
  {
    name: 'Туфли на каблуке со стразами',
    price: '4000',
    brand: 'ITALIANO',
    rating: '4.9 (59)',
    image: '/assets/Images/Shoes5.png',
    link: '/product/heels',
  },
];
</script>

<style scoped>
@import url('https://fonts.googleapis.com/css2?family=Roboto:wght@400;500;700&display=swap');

.about-page {
  font-family: 'Roboto', sans-serif;
  padding: 60px 0 100px;
  display: flex;
  flex-direction: column;
  align-items: center;
  gap: 60px;
}

.about-card {
  width: min(1320px, 92vw);
  background: #f7d4df;
  border: 5px solid #ff6f92;
  border-radius: 22px;
  padding: 60px 70px;
  box-shadow: 0 20px 60px rgba(0, 0, 0, 0.08);
}

.page-title {
  font-size: 40px;
  font-weight: 700;
  color: #1a1a1a;
  margin: 0 0 32px 0;
  text-align: left;
}

.about-text {
  display: grid;
  gap: 26px;
  font-size: 26px;
  line-height: 1.5;
  color: #1a1a1a;
}

.popular {
  width: 100%;
  background: linear-gradient(180deg, #ffb0c8 0%, #ff7ea5 100%);
  padding: 40px 0 80px;
  display: flex;
  flex-direction: column;
  align-items: center;
  box-shadow: inset 0 12px 24px rgba(0, 0, 0, 0.05);
}

.popular h2 {
  font-size: 34px;
  font-weight: 700;
  color: #1a1a1a;
  margin-bottom: 28px;
}

.popular__grid {
  width: min(1340px, 96vw);
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(260px, 1fr));
  gap: 28px;
}

.popular-card {
  background: #ffd7e3;
  border-radius: 18px;
  padding: 16px;
  display: flex;
  flex-direction: column;
  gap: 12px;
  box-shadow: 0 14px 28px rgba(0, 0, 0, 0.08);
  border: 3px solid #f6b0c6;
  transition: transform 0.2s ease, box-shadow 0.2s ease;
}

.popular-card:hover {
  transform: scale(1.02);
  box-shadow: 0 18px 34px rgba(0, 0, 0, 0.12);
}

.popular-card__image {
  background: #f5c3d3;
  border-radius: 12px;
  padding: 12px;
  display: flex;
  justify-content: center;
  align-items: center;
  min-height: 200px;
}

.popular-card__image img {
  width: 100%;
  height: 100%;
  object-fit: contain;
  border-radius: 8px;
}

.popular-card__content {
  display: flex;
  flex-direction: column;
  gap: 6px;
  color: #1a1a1a;
}

.popular-card__price-row {
  display: flex;
  justify-content: space-between;
  align-items: center;
  font-weight: 700;
  font-size: 18px;
}

.price {
  color: #000;
}

.brand {
  color: #444;
  font-weight: 500;
}

.popular-card__name {
  font-size: 16px;
  font-weight: 500;
  margin: 0;
}

.popular-card__rating {
  font-size: 14px;
  color: #5a3a3f;
  margin: 0;
}

.popular-card__btn {
  background: #ff5f90;
  color: #1a0c13;
  border: none;
  border-radius: 10px;
  padding: 12px 14px;
  font-size: 17px;
  font-weight: 700;
  cursor: pointer;
  transition: 0.2s ease;
  text-align: center;
  text-decoration: none;
  display: block;
}

.popular-card__btn:hover {
  background: #ff3f7c;
  transform: scale(1.03);
}
</style>
