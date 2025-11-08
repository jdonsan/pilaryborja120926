<template>
  <section class="my-details">
    <h2>Los detalles</h2>

    <article>
      <img class="flowers" src="@/assets/img/flores.webp" alt="flores icon" />
      <h3>Transporte</h3>

      <img class="icon" src="@/assets/img/autobus.svg" alt="bus icon" />
      <p>
        Habrá servicio de autobús para trasladaros desde diferentes puntos de
        Guadalajara hasta Montealvar, así como para el regreso al finalizar la
        celebración.
      </p>
      <p>
        Si prefieres venir en tu propio coche, no te preocupes: disponemos de
        parking privado exclusivo para los invitados.
      </p>
      <button>Paradas</button>
    </article>

    <article>
      <h3>Alojamiento</h3>

      <img class="icon" src="@/assets/img/cama.svg" alt="cama icon" />

      <p>
        Podréis alojaros en una de las habitaciones de Montealvar para disfrutar
        del entorno y la comodidad de estar en el mismo lugar de la celebración.
      </p>
      <p>
        Si lo preferís, también tenéis la opción de hospedaros en el hotel PAX
        (****), en el centro de Guadalajara.
      </p>
      <p>Para ambas opciones tenéis un 10% de descuento exclusivo.</p>
    </article>
  </section>
</template>

<script>
export default {
  name: 'MyDetails'
}
</script>
<style lang="scss" scoped>
.my-details {
  background: url('@/assets/img/curva-2.svg') center top no-repeat;
  padding: 96px 0 48px;

  article {
    position: relative;
    background-color: #fff;
    padding: 40px 25px;
    border-radius: 20px;
    max-width: 80%;
    margin: 0 auto 48px;
    box-shadow: 0px 0px 15px 0px $color-2;
    text-align: center;

    .flowers {
      width: 195px;
      position: absolute;
      top: -65px;
      left: -65px;
    }

    .icon {
      width: 60px;
      margin: 20px 0;
      filter: brightness(0) saturate(100%) invert(42%) sepia(8%) saturate(1163%)
        hue-rotate(235deg) brightness(92%) contrast(90%);
    }
  }

  h2 {
    font-family: $font-1;
    font-weight: $weight-font-bold;
    color: $color-1;
    width: 100%;
    font-size: 45px;
    line-height: 45px;
    margin-bottom: 66px;
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
    font-weight: $weight-font-regular;
    font-size: 16px;
    margin-bottom: 25px;
    line-height: 24px;
  }
}
</style>
