<template>
  <section id="photos" class="my-photos">
    <div class="my-photos-container">
      <h2>Las Fotos y Las Cervezas</h2>
      <h3>Universidad Cisneriana</h3>
      <my-container-center>
        <my-tag>
          <font-awesome-icon icon="fa-solid fa-clock" /> 19:00 - 21:00
        </my-tag>
      </my-container-center>

      <p>
        Una vez que hayamos dado el 'Sí, Quiero!', es momento de
        <b>hacernos fotos</b>.
      </p>
      <p>
        Nos acercaremos un momento a la <b>Plaza de San Diego</b> donde se
        encuentra la bonita fachada de la Universidad de Alcalá para hacernos
        algunas fotos allí y en los alrededores tanto en pareja como con
        vosotros y vosotras.
      </p>

      <my-container-center>
        <my-link href="https://goo.gl/maps/DvkzAraH1rgjTXwx9" target="_blank">
          <font-awesome-icon icon="fa-solid fa-location-dot" /> Ver Ubicación
        </my-link>
      </my-container-center>
      <br />
      <br />
      <br />

      <h3>Anexo Café-Bistró</h3>

      <img src="@/assets/img/beer.jpg" alt="Anexo Café-Bistró" />

      <p>
        Para calmar un poco las emociones, nos
        <b>tomaremos unas cervezas</b> cerca de la plaza para ir haciendo hambre
        antes de la cena.
      </p>

      <my-container-center>
        <my-link href="https://goo.gl/maps/7am8vVazQKhFmAGW8" target="_blank">
          <font-awesome-icon icon="fa-solid fa-location-dot" /> Ver Ubicación
        </my-link>
        <my-link
          href="http://hostelcomplutum.com/anexo-cafe-bistro/"
          target="_blank"
        >
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
  name: 'MyPhotos',

  components: {
    MyContainerCenter,
    MyTag,
    MyLink
  }
}
</script>

<style lang="scss">
.my-photos {
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
