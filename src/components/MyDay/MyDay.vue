<template>
  <section class="my-day">
    <div class="my-day-rings">
      <img src="@/assets/img/rings.svg" alt="Anillos" />
    </div>

    <div>
      <h2>El Gran Día</h2>
    </div>
  </section>
</template>

<script>
export default {
  name: 'MyDay'
}
</script>

<style lang="scss" scoped>
.my-day {
  &-rings {
    background: url('@/assets/img/curva-5.svg') center center no-repeat;
    position: relative;
    height: 200px;
    margin-bottom: 32px;

    img {
      width: 200px;
      height: 200px;
      position: absolute;
      left: 50%;
      transform: translateX(-50%);
    }
  }

  h2 {
    font-family: $font-1;
    font-weight: $weight-font-bold;
    color: $color-1;
    width: 100%;
    font-size: 45px;
    line-height: 45px;
    margin-bottom: 32px;
    text-align: center;
    width: 100%;
  }
}
</style>
