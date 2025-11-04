<template>
  <section class="my-cover">
    <div class="my-cover-container">
      <div class="my-cover-picture"></div>
      <div class="my-cover-content">
        <div class="my-cover-content-container">
          <span class="my-cover-date">12-IX-2026</span>
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
  position: relative;
  
  &-container {
    position: relative;
    margin: 0 auto;
    height: 800px;
  }

  &-picture {
    position: absolute;
    width: 100%;
    max-width: 768px;
    height: 450px;
    background-image: url('@/assets/img/bg.webp');
    background-position: center center;
    background-repeat: no-repeat;
    background-size: cover;
    background-attachment: fixed;
    z-index: 1;
  }

  &-content {
    position: relative;
    left: 0;
    right: 0;
    background: $color-5;
    z-index: 2;
    top: 450px;

    &::before {
      background-image: url('@/assets/img/curva-1.png');
      position: absolute;
      content: '';
      background-size: contain !important;
      background-repeat: no-repeat;
      background-position: top center;
      height: 100%;
      width: 100%;
      left: 0;
      top: -75px;
    }

    &-container {
      padding-top: 20px;
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
    padding: 5px 30px;
    margin-bottom: 35px;
    margin-top: 40px;
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
