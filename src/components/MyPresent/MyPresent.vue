<template>
  <section class="my-present">
    <h2>Los regalos</h2>
    <img class="icon" src="@/assets/img/regalo.svg" alt="icono regalo" />
    <p>
      Tu compañía es el mejor regalo, pero si deseas contribuir, puedes hacerlo
    </p>
    <button @click="openModal">Aquí</button>

    <div class="my-present-modal" v-if="isModalOpen">
      <div class="my-present-modal-overlay"></div>
      <div class="my-present-modal-content">
        <img class="flowers" src="@/assets/img/flores.webp" alt="flores icon" />
        <span class="my-present-modal-close" @click="closeModal">&times;</span>

        <div class="my-present-modal-icon">
          <img class="icon" src="@/assets/img/regalo.svg" alt="icono regalo" />
        </div>

        <h3>Nuestra cuenta</h3>
        <p>{{ iban }}</p>
      </div>
    </div>
  </section>
</template>

<script>
export default {
  name: 'MyPresent',

  data() {
    return {
      isModalOpen: false,
      iban: 'ES12 3456 7890 1234 5678 9012'
    }
  },

  methods: {
    openModal() {
      this.isModalOpen = true
    },

    closeModal() {
      this.isModalOpen = false
    }
  }
}
</script>

<style lang="scss" scoped>
.my-present {
  background: url('@/assets/img/curva-6.svg') center top no-repeat;
  padding: 96px 0 48px;
  text-align: center;

  h2 {
    font-family: $font-1;
    font-weight: $weight-font-bold;
    color: $color-1;
    width: 100%;
    font-size: 45px;
    line-height: 45px;
    margin-bottom: 36px;
    margin-top: 16px;
    text-align: center;
    width: 100%;
  }

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

  .icon {
    width: 60px;
    margin: 0 0 20px;
    filter: brightness(0) saturate(100%) invert(42%) sepia(8%) saturate(1163%)
      hue-rotate(235deg) brightness(92%) contrast(90%);
  }

  &-modal {
    &-overlay {
      position: fixed;
      top: 0;
      left: 0;
      width: 100%;
      height: 100%;
      background: rgba(116, 97, 126, 0.8);
      z-index: 999;
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
      z-index: 1000;
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

    &-close {
      position: absolute;
      top: -4px;
      right: 12px;
      font-size: 24px;
      cursor: pointer;
      background: $color-2;
      color: #fff;
      border-radius: 50%;
      width: 40px;
      height: 40px;
      display: flex;
      align-items: center;
      justify-content: center;
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
}
</style>
