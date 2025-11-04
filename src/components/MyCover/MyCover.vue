<template>
  <section class="my-cover">
    <div class="my-cover-picture"></div>
    <div class="my-cover-container">
      <div class="my-cover-content">
        <span class="my-cover-date">12-IX-2026</span>
        <h1 class="my-cover-names">
          Pilar
          <br />
          <span>&</span>
          <br />
          Borja
        </h1>
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
  position: relative;

  &-picture {
    position: fixed;
    width: 100%;
    max-width: 768px;
    height: 450px;
    background: url('@/assets/img/bg.webp') no-repeat center center/cover;
    z-index: 1;
  }

  &-container {
    position: relative;
    background: $color-5;
    padding-top: 450px;

    &::before {
      background-image: url('@/assets/img/curva-1.png');
      position: absolute;
      content: '';
      background-size: contain !important;
      background-repeat: no-repeat;
      background-position: bottom center;
      height: 100%;
      width: 100%;
      z-index: 2;
      left: 0;
      top: 0;
    }
  }

  &-content {
    position: absolute;
    left: 0;
    right: 0;
    z-index: 999;
    top: 450px;
    background: $color-5;
    padding-bottom: 20px;
  }

  &-date {
    font-size: 25px;
    display: flex;
    justify-content: center;
    align-items: center;
    font-family: $font-2;
  }

  &-names {
    font-size: 100px;
    color: $color-1;
    font-family: $font-1;
    font-weight: $weight-font-regular;
    line-height: 69px;

    span {
      font-size: 35px;
      font-family: $font-2;
      display: inline-flex;
      justify-content: center;
      align-items: center;
      width: 50px;
      height: 50px;
      background: $color-2;
      color: $color-4;
      border-radius: 100%;
      margin-bottom: 15px;
    }
  }

  &-line {
    display: block;
    border-top: 1px solid $color-2;
    margin: 0 auto;
    margin-top: 2rem;
    width: 50%;
  }
}
</style>
