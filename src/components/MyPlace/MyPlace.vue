<template>
  <section class="my-place">
    <h2>El Lugar</h2>

    <div class="my-place-picture">
      <img src="@/assets/img/finca.jpg" alt="Finca Montealvar" />
      <img
        class="curva"
        src="@/assets/img/curva-4.svg"
        alt="Finca Montealvar"
      />
    </div>

    <div class="my-place-content">
      <h3>Finca Montealvar</h3>

      <p>
        La boda se celebrará en la preciosa finca de Montealvar, situada en el
        corazón del bosque de Valdenazar, a las afueras de Guadalajara.
      </p>
      <p>
        Es un entorno natural con vistas al campo de golf y jardines románticos,
        perfecto para disfrutar en compañía de todos vosotros de un día tan
        especial para nosotros.
      </p>

      <h4>DIRECCIÓN</h4>
      <p>Monasterio de Alcohete, Yebes (Guadalajara)</p>
      <my-link
        target="_blank"
        href="https://www.google.com/maps/dir/?api=1&destination=Montealvar, Monasterio de Alcohete, s/n, 19139, Guadalajara"
      >
        ¿Cómo llegar?
      </my-link>
    </div>
  </section>
</template>

<script>
import MyLink from '@/components/MyLink/MyLink'

export default {
  name: 'MyPlace',
  components: {
    MyLink
  }
}
</script>

<style lang="scss" scoped>
.my-place {
  background: url('@/assets/img/curva-2.svg') center top no-repeat;
  padding: 96px 0;
  margin: 32px 0;
  text-align: center;

  &-picture {
    width: 100%;
    text-align: center;
    margin-bottom: 32px;
    position: relative;

    &::before {
      background-image: url('@/assets/img/curva-3.svg');
      position: absolute;
      content: '';
      background-repeat: no-repeat;
      background-position: top center;
      height: 100%;
      width: 100%;
      top: -32px;
      z-index: 99;
    }

    .curva {
      position: absolute;
      left: 0;
      bottom: 0;
      z-index: 99;
    }
  }

  &-content {
    margin: 0 auto;
    padding: 0 15px;
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

  h3 {
    font-family: $font-2;
    text-align: center;
    font-size: 20px;
    color: $color-2;
    font-size: 25px;
    margin-bottom: 16px;
  }

  h4 {
    font-family: $font-2;
    font-weight: $weight-font-bold;
    color: $color-1;
    font-size: 25px;
    text-transform: uppercase;
    margin-bottom: 8px;
  }

  p {
    text-align: center;
    font-family: $font-2;
    color: $color-3;
    font-weight: $weight-font-light;
    font-size: 19px;
    margin-bottom: 25px;
    line-height: 1.5;
  }
}
</style>
