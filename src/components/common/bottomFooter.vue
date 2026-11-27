<template>
  <footer id="VISIT" class="visit">
    <h2>Make an appointment</h2>
    <div class="visit__grid">
      <p class="visit__mark">Yoomi Nail &amp; Spa</p>
      <div>
        <h3>Business Hours</h3>
        <p>Monday – Saturday: 12:00PM – 7:00PM</p>
        <p>Sunday: 12:00PM – 6:00PM</p>
        <h3>Location</h3>
        <p>133-55 Roosevelt Ave, 2nd floor, Flushing, NY 11354</p>
        <h3>Contact</h3>
        <p>Tel.: <a href="tel:646-379-9995">646-379-9995</a></p>
        <div class="visit__social">
          <a href="https://www.facebook.com/tattoo7traintattoo" target="_blank" rel="noreferrer">Facebook</a>
          <a href="https://www.instagram.com/7traintattoo" target="_blank" rel="noreferrer">Instagram</a>
        </div>
      </div>
    </div>
    <div class="visit__bar">© 2026 Yoomi Nail Spa. All Rights Reserved. x WAG Marketing</div>
  </footer>
</template>

<style lang="scss" scoped>
.visit {
  background: #333333;
  color: #ffffff;
  padding: 72px 40px 0;

  h2 {
    margin: 0 0 48px;
    color: #0fa2ad;
    text-align: center;
    font-family: var(--display-font), "Playfair Display", serif;
    font-size: 40px;
    font-weight: 700;
    line-height: 1.32;
  }

  &__grid {
    display: flex;
    justify-content: center;
    gap: 80px;
    align-items: flex-start;
    padding-bottom: 72px;
  }

  h3 {
    margin: 28px 0 8px;
    font-family: var(--display-font), "Playfair Display", serif;
    font-size: 20px;
    font-weight: 700;
    line-height: 28px;
  }

  p,
  a {
    margin: 0;
    color: #ffffff;
    font-family: "InriaSans", "Noto Sans", sans-serif;
    font-size: 16px;
    font-weight: 400;
    line-height: 22.4px;
    text-decoration: none;
  }

  .visit__mark {
    margin: 0;
    max-width: 280px;
    color: #ffffff;
    font-family: var(--display-font), "Playfair Display", serif;
    font-size: 40px;
    font-weight: 700;
    line-height: 1.2;
  }

  &__social {
    display: flex;
    gap: 16px;
    margin-top: 16px;
  }

  &__bar {
    margin: 0 -40px;
    height: 85px;
    display: flex;
    align-items: center;
    justify-content: center;
    background: #e394a4;
    color: #000000;
    font-family: "InriaSans", "Noto Sans", sans-serif;
    font-size: 14px;
    text-align: center;
    padding: 0 16px;
  }
}

@media (max-width: 800px) {
  .visit {
    padding: 48px 20px 0;

    h2 {
      font-size: 32px;
    }

    &__grid {
      flex-direction: column;
      align-items: center;
      text-align: center;
      gap: 32px;
    }

    &__social {
      justify-content: center;
    }

    &__bar {
      margin: 0 -20px;
      height: auto;
      min-height: 85px;
    }
  }
}
</style>
