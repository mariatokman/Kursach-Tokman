<template>
    <section class="hero">
        <div class="hero__text">
            <h1>
                Розовая одежда – это широкий выбор от нежных пастельных тонов до сочных фуксий.
                Найдите свой идеальный оттенок в нашей коллекции
            </h1>

            <router-link to="/catalog"><button class="hero__btn">Вперед за покупками</button></router-link>
        </div>

        <img src="/assets/Images/Woman.png" class="hero__img" alt="Женщина">
    </section>
    <img src="/assets/Images/Line.png" alt="Линия">
    <section class="blocks">

        <!-- ШУБЫ -->
        <div class="block ">
            <div class="block__text">
                <h2>
                    Наши шубы – это роскошь, которая дарит не только стиль, но и удивительную лёгкость
                </h2>
            </div>

            <div class="circle">
                <img src="/assets/Images/Coat.png" alt="Шуба">
            </div>
        </div>

        <!-- КРОССОВКИ -->
        <div class="block ">
            <div class="circle">
                <img src="/assets/Images/Snickers.png" alt="Кроссовки">
            </div>

            <div class="block__text">
                <h2>
                    Наши кроссовки – это идеальное сочетание комфорта и лёгкости
                </h2>
            </div>
        </div>

        <!-- ЮБКИ -->
        <div class="block">
            <div class="block__text">
                <h2>
                    Наши юбки – это изысканный силуэт, в котором вы почувствуете себя невесомой
                </h2>
            </div>

            <div class="circle">
                <img src="/assets/Images/Skirt.png" alt="Юбка">
            </div>
        </div>

        <section class="fabric-block">
            <div class="fabric-block__content">
                <h2>О наших тканях</h2>
                <p>Мы используем только натуральные ткани премиум-класса:</p>
                <ul>
                    <li><strong>Шёлк</strong> — плотный, матовый, идеально держит форму.</li>
                    <li><strong>Кашемир</strong> — невесомый, не скатывается, дарит облачное тепло.</li>
                    <li><strong>Хлопок</strong> — чем дольше носишь, тем он мягче.</li>
                    <li><strong>Лён</strong> — создаёт прохладу, благородно мнётся.</li>
                    <li><strong>Тенсель (из эвкалипта)</strong> — шелковистый, экологичный, дышит.</li>
                </ul>
                <p>Любую вещь мы можем адаптировать в индивидуальном порядке — скроем и скорректируем именно под вашу фигуру для идеальной посадки.</p>
                <p>Это инвестиция в комфорт, долговечность и безупречный вид каждый день.</p>
            </div>
            <div class="fabric-block__image">
                <img class="fabric-block__img" src="/assets/Images/Tkan.png" alt="Ткани">
            </div>
        </section>

        <Email />
    </section>
</template>

<script setup>
import Email from "../Components/Email.vue";
</script>

<style scoped>
@import url('https://fonts.googleapis.com/css2?family=Prosto+One&family=Roboto:ital,wght@0,100..900;1,100..900&display=swap');
/* ------- HERO SECTION ------- */

.hero {
    display: flex;
    justify-content: space-between;
    align-items: center;
    padding: 0px 120px;
    background: linear-gradient(#e6d0d4, #C9A1A8);
}

.hero__text {
    font-family: "Prosto One", sans-serif;
    max-width: 900px;
}

.hero__text h1 {
    font-size: 45px;
    font-weight: 700;
    line-height: 1.3;
    margin-bottom: 30px;
    color: #4a0c22;
}

.hero__btn {
    font-family: "Prosto One", sans-serif;
    background: #fc7f9c;
    color: #4a0c22;
    border: none;
    padding: 14px 28px;
    border-radius: 6px;
    font-size: 20px;
    cursor: pointer;
    transition: 0.3s;
}

.hero__btn:hover {
    background: #ff325f;
}

.hero__img {
    width: 700px;
}

/* ------- BLOCKS ------- */

.blocks {
    padding: 80px 120px;
}

.block {
    display: flex;
    align-items: center;
    justify-content: space-between;
    margin-bottom: 120px;
}

.block--reverse {
    flex-direction: row-reverse;
}

.block__text {
    font-family: "Prosto One", sans-serif;
    width: 45%;
}

.block__text h2 {
    font-size: 40px;
    line-height: 1.4;
    color: #4a0c22;
    font-weight: 700;
}

.circle {
    width: 500px;
    height: 500px;
    border-radius: 50%;
    display: flex;
    justify-content: center;
    align-items: center;
}

.circle img { 
    width: 100%;
    height: auto;
}

img {
  display: block;
}

/* ------- FABRIC BLOCK ------- */

.fabric-block {
    display: grid;
    grid-template-columns: 1fr 1fr;
    gap: 40px;
    align-items: center;
    padding: 60px 80px;
    background: #ff879c;
    border-radius: 24px;
    color: #4a0c22;
    font-family: "Prosto One", sans-serif;
    margin-bottom: 100px;
}

.fabric-block__content h2 {
    font-size: 42px;
    margin-bottom: 16px;
}

.fabric-block__content p {
    font-size: 20px;
    line-height: 1.5;
    margin-bottom: 12px;
}

.fabric-block__content ul {
    list-style: none;
    padding: 0;
    margin: 0 0 16px 0;
    display: grid;
    gap: 8px;
}

.fabric-block__content li {
    font-size: 19px;
    line-height: 1.4;
    padding-left: 0;
}

.fabric-block__image {
    width: 100%;
    height: 100%;
    display: flex;
    justify-content: center;
    align-items: center;
}

.fabric-block__img {
    width: 100%;
    max-width: 520px;
    height: 590px;
    aspect-ratio: 4 / 3;
    object-fit: cover;
    border-radius: 18px;
    border: 6px solid #4a0c22;
    background: #f5d8df;
}
</style>