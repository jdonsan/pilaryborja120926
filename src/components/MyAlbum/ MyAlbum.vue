<template>
  <section class="my-album">
    <div class="my-album-picture">
      <img
        class="curva"
        src="@/assets/img/curva-4.svg"
        alt="Finca Montealvar"
      />
    </div>

    <div class="my-album-container">
      <div class="my-album-content">
        <h2>Compartimos este día junto a ti</h2>

        <p>Comparte tus fotos y vídeos de este inolvidable día</p>

        <img class="my-album-icon" src="@/assets/img/icon.png" alt="Icon" />
        <h3>#pilaryborja</h3>

        <my-link target="_blank" href="https://photos.app.goo.gl/XYZ12345ABCD">
          Ir a Álbum
        </my-link>
      </div>
    </div>
  </section>
</template>

<script>
import MyLink from '@/components/MyLink/MyLink'

export default {
  name: 'MyAlbum',
  components: {
    MyLink
  }
}
</script>

<style lang="scss" scoped>
.my-album {
  padding: 40px 0 48px;
  margin: 32px 0 128px;
  text-align: center;
  position: relative;
  height: 600px;

  &-icon {
    width: 100px;
    margin: 0 auto 10px;
  }

  &-picture {
    width: 100%;
    height: 600px;
    text-align: center;
    margin-bottom: 32px;
    position: absolute;
    background-image: url('@/assets/img/bg-2.webp');
    background-position: center center;
    background-repeat: no-repeat;
    background-size: cover;
    background-attachment: fixed;

    .curva {
      position: absolute;
      left: 0;
      bottom: -1px;
      z-index: 99;
    }
  }

  &-container {
    margin: 0 auto;
    position: absolute;
    background: rgba($color-1, 0.7);
    height: 100%;
    width: 100%;

    &::before {
      background-image: url('@/assets/img/curva-3.svg');
      position: absolute;
      content: '';
      background-repeat: no-repeat;
      background-position: top center;
      height: 100%;
      width: 100%;
      left: 0;
      right: 0;
      top: -32px;
      z-index: 100;
    }

    .my-album-content {
      position: absolute;
      display: flex;
      flex-direction: column;
      align-items: center;
      justify-content: center;
      z-index: 200;
      width: 100%;
      height: 100%;
      padding: 0 15px;
    }
  }

  h2 {
    font-family: $font-1;
    font-weight: $weight-font-bold;
    color: #fff;
    width: 100%;
    font-size: 45px;
    line-height: 45px;
    margin-bottom: 36px;
    text-align: center;
    width: 100%;
  }

  h3 {
    font-family: $font-2;
    text-align: center;
    font-size: 20px;
    color: #fff;
    font-size: 29px;
    margin-bottom: 16px;
  }

  p {
    text-align: center;
    font-family: $font-2;
    color: #fff;
    font-weight: $weight-font-light;
    font-size: 19px;
    line-height: 1.5;
    width: 95%;
    margin: 0 auto 25px;
  }
}
</style>
