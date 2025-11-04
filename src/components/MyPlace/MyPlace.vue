<template>
  <section id="place" class="my-place">
    <div class="my-place-container">
      <h2>El Lugar</h2>
      <h3>Alcalá de Henares</h3>
      <img src="@/assets/img/alcala.jpeg" alt="" />
      <p>
        Después de 10 años, 8.124 paseos, 1.280 comidas, 500 películas, 50
        conciertos, infinitas celebraciones, después de 9 años viviendo juntos,
        después de tantos y tantos buenos momentos compartidos y, sobre todo,
        después de tanta expectativa creada, el gran día llega...
        <b>¡Nos casamos!</b>
      </p>
      <p>
        Os invitamos a un fin de semana diferente en Alcalá de Henares,
        Patrimonio de la Humanidad, para
        <b>celebrar nuestro amor y vuestro cariño</b>. Un fin de semana para
        comer y beber, reir y llorar, bailar y descansar, para aprender, conocer
        y no parar... en definitiva, un fin de semana para disfrutar.
      </p>
      <p>
        Queremos que <b>aprovechéis</b> este fin de semana para conocer más a
        nuestras familias, para que redescubráis a vuestras parejas o amigos y
        para que guardéis un día especial en vuestros recuerdos. Estad atentos a
        todo lo que tenemos planeado para vosotros y vosotras.
      </p>

      <my-container-center>
        <my-link href="https://goo.gl/maps/aSKrSJ57gJDZuP9T9" target="_blank">
          <font-awesome-icon icon="fa-solid fa-location-dot" /> Ver Ubicación
        </my-link>
        <my-link
          href="https://es.wikipedia.org/wiki/Alcal%C3%A1_de_Henares"
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
import MyLink from '@/components/MyLink/MyLink'

export default {
  name: 'MyPlace',

  components: {
    MyContainerCenter,
    MyLink
  }
}
</script>

<style lang="scss">
.my-place {
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
