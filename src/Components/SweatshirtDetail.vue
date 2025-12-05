<template>
  <section class="detail">
    <div class="detail__card">
      <div class="detail__image">
        <img src="/assets/Images/Shirt5.png" alt="Свитшот осенний" />
      </div>
      <div class="detail__content">
        <p class="detail__brand">Пальмира</p>
        <h1>Свитшот осенний</h1>
        <p class="detail__price">2000 ₽</p>
        <p class="detail__desc">
          Лёгкий утеплённый свитшот с авторским принтом, мягкими манжетами и удобной свободной посадкой.
          Сохраняет форму, не образует катышков и дарит комфорт в межсезонье.
        </p>
        <ul class="detail__list">
          <li><strong>Состав:</strong> хлопок 80%, полиэстер 20%</li>
          <li><strong>Плотность:</strong> 320 г/м², мягкий флис внутри</li>
          <li><strong>Крой:</strong> oversize, опущенная линия плеч</li>
          <li><strong>Уход:</strong> стирка в деликатном режиме, не отбеливать</li>
        </ul>
        <button class="detail__btn">Добавить в корзину</button>
      </div>
    </div>
  </section>
</template>

<style scoped>
@import url('https://fonts.googleapis.com/css2?family=Roboto:wght@400;500;700&display=swap');

.detail {
  min-height: calc(100vh - 120px);
  display: flex;
  align-items: center;
  justify-content: center;
  padding: 80px 40px;
  font-family: 'Roboto', sans-serif;
}

.detail__card {
  width: min(1200px, 96vw);
  background: #f7d4df;
  border: 4px solid #ff6f92;
  border-radius: 24px;
  padding: 38px;
  display: grid;
  grid-template-columns: 1fr 1fr;
  gap: 30px;
  box-shadow: 0 24px 60px rgba(0, 0, 0, 0.12);
}

.detail__image {
  background: #000000;
  border-radius: 18px;
  padding: 5px;
  display: flex;
  justify-content: center;
  align-items: center;
}

.detail__image img {
  width: 100%;
  height: 100%;
  object-fit: contain;
  border-radius: 12px;
}

.detail__content {
  display: grid;
  gap: 12px;
  color: #1a1a1a;
}

.detail__brand {
  color: #7c4354;
  font-weight: 700;
  letter-spacing: 0.5px;
  margin: 0;
}

.detail__price {
  font-size: 32px;
  font-weight: 700;
  margin: 0;
}

.detail__desc {
  font-size: 17px;
  line-height: 1.55;
  margin: 6px 0 0 0;
}

.detail__list {
  list-style: none;
  padding: 0;
  margin: 0;
  display: grid;
  gap: 6px;
  font-size: 16px;
}

.detail__btn {
  background: #ff5f90;
  color: #1a0c13;
  border: none;
  border-radius: 12px;
  padding: 14px;
  font-size: 17px;
  font-weight: 700;
  cursor: pointer;
  transition: 0.2s ease;
  margin-top: 4px;
}

.detail__btn:hover {
  background: #ff3f7c;
  transform: translateY(-1px);
}

@media (max-width: 900px) {
  .detail__card {
    grid-template-columns: 1fr;
  }
}
</style>
