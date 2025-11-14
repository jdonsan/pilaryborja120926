<template>
  <div class="my-refresh">
    <div class="my-refresh-overlay"></div>
    <div class="my-refresh-content">
      <img class="flowers" src="@/assets/img/flores.webp" alt="flores icon" />

      <div class="my-refresh-icon">
        <img
          class="icon"
          src="@/assets/img/actualizar.svg"
          alt="icono actualizar"
        />
      </div>

      <p>Hay una nueva versión de la invitación</p>
      <button @click="() => $emit('refresh')">Actualizar</button>
    </div>
  </div>
</template>

<script>
export default {
  name: 'MyRefresh'
}
</script>

<style lang="scss" scoped>
.my-refresh {
  h3 {
    font-family: $font-2;
    text-align: center;
    font-size: 20px;
    color: $color-2;
    font-size: 25px;
    margin-bottom: 16px;
  }

  p {
    text-align: center;
    font-family: $font-2;
    color: $color-3;
    font-weight: $weight-font-light;
    font-size: 19px;
    line-height: 1.5;
    user-select: text;
    width: 95%;
    margin: 0 auto 25px;
  }

  &-overlay {
    position: fixed;
    top: 0;
    left: 0;
    width: 100%;
    height: 100%;
    background: rgba(116, 97, 126, 0.8);
    z-index: 99999;
  }

  &-content {
    position: fixed;
    top: 50%;
    left: 50%;
    transform: translate(-50%, -50%);
    background: #fff;
    padding: 30px;
    padding-top: 80px;
    border-radius: 40px;
    z-index: 100000;
    text-align: center;
    width: 90%;
    max-width: 400px;

    .flowers {
      width: 195px;
      position: absolute;
      top: -80px;
      left: -60px;
    }
  }

  &-icon {
    position: absolute;
    box-shadow: 0px 0px 15px 0px #444;
    border-radius: 50%;
    background: #fff;
    top: -50px;
    left: 50%;
    transform: translateX(-50%);
    width: 100px;
    height: 100px;
    display: flex;
    align-items: center;
    justify-content: center;

    .icon {
      width: 50px;
      margin: 0;
    }
  }
}
</style>
