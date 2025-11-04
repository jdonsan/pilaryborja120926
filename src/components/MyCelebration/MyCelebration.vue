<template>
  <section id="celebration" class="my-celebration">
    <div class="my-celebration-container">
      <h2>La Celebración</h2>
      <h3>Restaurante Casino</h3>

      <my-container-center>
        <my-tag>
          <font-awesome-icon icon="fa-solid fa-clock" /> 21:00 - 23:00
        </my-tag>
      </my-container-center>

      <p>
        Disfrutaremos de una <b>rica y variada</b> cena en este bonito
        restaurante de la ciudad.
      </p>
      <p>
        El restaurante se encuentra al lado del Ayuntamiento y del Parador, por
        lo que podréis estar a <b>menos de un minuto</b> de un sitio al otro sin
        tener que andar mucho.
      </p>
      <p>
        Aunque ya os lo hemos consultado, si alguno o alguna sois
        <b>intolerantes a algún alimento</b>, hacédnoslo saber para que lo
        tengamos en cuenta para ese día.
      </p>

      <my-container-center>
        <my-link href="https://goo.gl/maps/6zdEpQbh3uHfChrR6" target="_blank">
          <font-awesome-icon icon="fa-solid fa-location-dot" /> Ver Ubicación
        </my-link>
        <my-link href="https://www.casinoalcala.es/" target="_blank">
          <font-awesome-icon icon="fa-solid fa-circle-info" /> Saber Más
        </my-link>
      </my-container-center>
    </div>
  </section>
</template>

<script>
import MyContainerCenter from '@/components/MyContainerCenter/MyContainerCenter'
import MyTag from '@/components/MyTag/MyTag'
import MyLink from '@/components/MyLink/MyLink'

export default {
  name: 'MyCelebration',

  components: {
    MyContainerCenter,
    MyTag,
    MyLink
  }
}
</script>

<style lang="scss">
.my-celebration {
  background: $color-5;
  position: relative;

  &-container {
    margin: 0 auto;
    z-index: 999;
    position: relative;
    background: $color-5;
  }
}
</style>
