<template>
  <section class="my-cover">
    <div class="my-cover-container">
      <div class="my-cover-picture"></div>
      <div class="my-cover-content">
        <img src="@/assets/img/curva-1.png" alt="curva" />
        <div class="my-cover-content-container">
          <span class="my-cover-date">12.09.2026</span>
          <h1 class="my-cover-names">
            <span>Pilar</span>
            <span class="circle">&</span>
            <span>Borja</span>
          </h1>
        </div>
      </div>
    </div>
  </section>
</template>

<script>
export default {
  name: 'MyCover'
}
</script>

<style lang="scss" scoped>
.my-cover {
  text-align: center;

  &-container {
    margin: 0 auto;
  }

  &-picture {
    width: 100%;
    max-width: 768px;
    height: 120vw;
    background-image: url('@/assets/img/bg.jpg');
    background-position: top center;
    background-repeat: no-repeat;
    background-size: 100% auto;
    background-attachment: fixed;

    @media (min-width: 769px) {
      background-size: 768px auto;
      height: 612px;
    }
  }

  &-content {
    margin-top: -110px;
    padding-bottom: 92px;

    &-container {
      background-color: $color-5;
    }
  }

  &-date {
    display: flex;
    justify-content: center;
    align-items: center;
    font-family: $font-2;
    display: inline-block;
    white-space: nowrap;
    width: auto;
    font-family: $font-1;
    font-weight: $weight-font-regular;
    font-size: 25px;
    line-height: 25px;
    color: $color-3;
    padding: 4px 32px;
    margin: 16px auto 32px auto;
  }

  &-names {
    color: $color-1;
    font-family: $font-1;
    font-weight: $weight-font-bold;
    font-size: 70px;
    display: flex;
    flex-direction: column;
    justify-content: center;
    align-items: center;

    span {
      display: flex;
      width: 100%;
      justify-content: center;
      align-items: center;
    }

    .circle {
      position: relative;
      font-family: $font-1;
      display: flex;
      justify-content: center;
      align-items: center;
      background: $color-2;
      font-weight: $weight-font-regular;
      border-radius: 50%;
      width: 60px;
      height: 60px;
      font-size: 40px;
      color: #fff;

      &::before {
        content: '';
        left: 65px;
        background: $color-2;
        display: inline-block;
        position: absolute;
        top: 30px;
        width: 80px;
        height: 1px;
      }

      &::after {
        content: '';
        right: 65px;
        background: $color-2;
        display: inline-block;
        position: absolute;
        top: 30px;
        width: 80px;
        height: 1px;
      }
    }
  }
}
</style>
