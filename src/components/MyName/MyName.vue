<template>
  <section class="my-name">
    <h1 class="my-names">
      <span>Pilar</span>
      <span class="circle">&</span>
      <span>Borja</span>
    </h1>
  </section>
</template>

<style lang="scss" scoped>
.my-name {
  padding: 0 16px 64px;
  background: $color-5;
  text-align: center;
}

.my-names {
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
</style>
