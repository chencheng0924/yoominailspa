<template>
  <div>
    <section id="HOME" class="hero">
      <img src="@/assets/img/newJpg/WechatIMG75.jpg" alt="Pink chrome manicure">
      <div class="hero__copy">
        <h1>Yoomi Nail Spa</h1>
        <p>Hands, feet, and a quieter hour.</p>
      </div>
    </section>

    <section id="ABOUT" class="intro">
      <h2>Yoomi Nail Spa</h2>
      <p>Manicures and pedicures are the center of a visit. Color, shape, and nail care are chosen with you at the chair, then finished without a rush.</p>
      <p>The studio also holds time for soothing hand and foot care. A longer visit can pair nail work with a quiet break for tired hands.</p>
      <p>Waxing and brow shaping can be added to this list once the studio's own menu is ready. Each service will keep its real duration and price.</p>
      <p>Call 646-379-9995 to ask for a time, or stop by 133-55 Roosevelt Ave, 2nd floor, Flushing, NY 11354.</p>
    </section>

    <section class="band" aria-label="Studio photos">
      <img src="@/assets/img/newJpg/WechatIMG69.jpg" alt="Pink and lime nail art">
      <img src="@/assets/img/newJpg/WechatIMG70.jpg" alt="Neutral glazed manicure">
      <img src="@/assets/img/newJpg/WechatIMG71.jpg" alt="Black floral nail art">
      <img src="@/assets/img/newJpg/WechatIMG72.jpg" alt="Graphic manicure">
      <img src="@/assets/img/newJpg/WechatIMG73.jpg" alt="Red and black nail art">
      <img src="@/assets/img/newJpg/WechatIMG74.jpg" alt="Nail art over a speckled cup">
    </section>

    <section id="CARE" class="care">
      <div class="care__copy">
        <h2>Care, at your pace</h2>
        <p>Stations stay clean, and the appointment is yours from start to finish. Service names, timing, and prices will replace this note when the menu is final.</p>
      </div>
      <img src="@/assets/img/newJpg/WechatIMG47.jpg" alt="Yoomi Nail and Spa storefront">
    </section>
  </div>
</template>

<style lang="scss" scoped>
.hero {
  position: relative;
  height: 808px;
  background: #000000;
  overflow: hidden;

  img {
    width: 100%;
    height: 100%;
    object-fit: cover;
    object-position: center center;
  }

  &__copy {
    position: absolute;
    inset: 0;
    display: flex;
    flex-direction: column;
    align-items: center;
    justify-content: center;
    gap: 8px;
    padding: 0 24px;
    text-align: center;
    color: #ffffff;
  }

  h1,
  p {
    margin: 0;
    font-family: var(--display-font), "Playfair Display", serif;
    font-weight: 700;
  }

  h1 {
    max-width: 1006px;
    font-size: clamp(36px, 5.5vw, 79px);
    line-height: 1.4;
  }

  p {
    font-size: 28px;
    line-height: 1.4;
  }
}

.intro {
  max-width: 975px;
  margin: 0 auto;
  padding: 135px 24px 106px;

  h2 {
    margin: 0 0 42px;
    color: #000000;
    font-family: var(--display-font), "Playfair Display", serif;
    font-size: 56px;
    font-weight: 700;
    line-height: 1.34;
  }

  p {
    margin: 0 0 22px;
    color: #000000;
    font-family: "InriaSans", "Noto Sans", sans-serif;
    font-size: 16px;
    font-weight: 400;
    line-height: 22.4px;
  }
}

.band {
  display: grid;
  grid-template-columns: repeat(3, 1fr);
  gap: 16px;
  width: min(1360px, calc(100% - 80px));
  margin: 0 auto;
  padding: 48px;
  background: rgba(232, 192, 179, 0.34);

  img {
    width: 100%;
    height: 420px;
    object-fit: cover;
  }
}

.care {
  display: grid;
  grid-template-columns: 1.1fr 0.9fr;
  gap: 48px;
  align-items: center;
  max-width: 1200px;
  margin: 0 auto;
  padding: 106px 24px 120px;

  h2 {
    margin: 0 0 24px;
    color: #000000;
    font-family: var(--display-font), "Playfair Display", serif;
    font-size: 56px;
    font-weight: 700;
    line-height: 1.4;
  }

  p {
    margin: 0;
    max-width: 560px;
    color: #000000;
    font-family: "InriaSans", "Noto Sans", sans-serif;
    font-size: 16px;
    line-height: 22.4px;
  }

  img {
    width: 100%;
    height: 460px;
    object-fit: cover;
  }
}

@media (max-width: 949px) {
  .band {
    grid-template-columns: 1fr 1fr;
    width: calc(100% - 32px);
    padding: 24px;
  }

  .care {
    grid-template-columns: 1fr;
    padding: 64px 24px;
  }
}

@media (max-width: 640px) {
  .hero {
    height: 520px;

    p {
      font-size: 18px;
      line-height: 26px;
    }
  }

  .intro {
    padding: 64px 20px 48px;

    h2 {
      font-size: 36px;
    }
  }

  .band {
    grid-template-columns: 1fr;

    img {
      height: 240px;
    }
  }

  .care h2 {
    font-size: 36px;
  }
}
</style>
