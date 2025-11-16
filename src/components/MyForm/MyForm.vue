<template>
  <section class="my-form">
    <h2 id="my-form">¡Tu confirmación es muy importante!</h2>
    <img class="icon" src="@/assets/img/form.svg" alt="icono formulario" />
    <p>
      Nos ayudaría mucho que rellenases el siguiente formulario para organizar
      un día inolvidable.
    </p>
    <button @click="toggle">
      {{ isFormOpen ? 'Cerrar' : 'Rellenar' }}
    </button>

    <div class="my-form-content" v-if="isFormOpen">
      <iframe
        src="https://docs.google.com/forms/d/e/1FAIpQLSelmOVbq_sP-vmpyctCRWmyhYH-9PXMFBm926kQ3icltyrbsg/viewform?embedded=true"
        width="100%"
        height="1650"
        frameborder="0"
        marginheight="0"
        marginwidth="0"
      >
        Cargando…
      </iframe>
    </div>
  </section>
</template>

<script>
export default {
  name: 'MyForm',

  data() {
    return {
      isFormOpen: false
    }
  },

  methods: {
    toggle() {
      this.isFormOpen = !this.isFormOpen
      this.$nextTick(() => {
        this.scrollToForm()
      })
    },

    scrollToForm() {
      const element = document.getElementById('my-form')
      element.scrollIntoView({ top: 0, behavior: 'smooth' })
    }
  }
}
</script>

<style lang="scss" scoped>
.my-form {
  background: url('@/assets/img/curva-2.svg') center top no-repeat;
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

  .my-form-content {
    margin-top: 32px;
  }
}
</style>
