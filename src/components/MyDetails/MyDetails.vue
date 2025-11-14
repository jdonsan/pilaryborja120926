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
      <button @click="openModal">Paradas</button>
    </article>

    <article>
      <h3>Alojamiento</h3>

      <img class="icon" src="@/assets/img/cama.svg" alt="cama icon" />

      <p>
        Podréis alojaros en una de las habitaciones de Montealvar para disfrutar
        del entorno y la comodidad de estar en el mismo lugar de la celebración.
      </p>
      <p>
        Si lo preferís, también tenéis la opción de hospedaros en el Hotel PAX
        (4*), en el centro de Guadalajara.
      </p>
      <p>Para ambas opciones tenéis un 10% de descuento exclusivo.</p>

      <my-link
        href="https://paxhoteles.com/hotel-pax-guadalajara/"
        target="_blank"
        rel="noopener noreferrer"
      >
        Ver Hotel PAX
      </my-link>
    </article>

    <div class="my-details-modal" v-if="isModalOpen">
      <div class="my-details-modal-overlay" @click="closeModal"></div>
      <div class="my-details-modal-content">
        <img class="flowers" src="@/assets/img/flores.webp" alt="flores icon" />
        <span class="my-details-modal-close" @click="closeModal">&times;</span>

        <div class="my-details-modal-icon">
          <img
            class="icon"
            src="@/assets/img/autobus.svg"
            alt="icono autobús"
          />
        </div>

        <h3>Paradas</h3>
        <ul class="my-details-steps">
          <li
            class="my-details-steps-item"
            v-for="(item, index) in steps"
            :key="index"
          >
            <div class="my-details-steps-item-content">
              <p>{{ item.name }}</p>
              <h3>{{ item.dir }}</h3>
            </div>
          </li>
        </ul>
      </div>
    </div>
  </section>
</template>

<script>
import MyLink from '@/components/MyLink/MyLink'

export default {
  name: 'MyDetails',

  components: {
    MyLink
  },

  data() {
    return {
      isModalOpen: false,
      steps: [
        {
          name: 'Palacio del Infantado',
          dir: 'Plaza de España, 13'
        },
        {
          name: 'Colegio Salesianos',
          dir: 'Calle Toledo, 24'
        },
        {
          name: 'Iglesia de San Diego de Alcalá',
          dir: 'Avenida de El Atance, 1'
        }
      ]
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

  &-steps {
    display: inline-block;

    &-item {
      display: flex;
      align-items: center;
      position: relative;
      $size: 16px;
      border-left: 3px solid $color-2;

      &::before {
        content: '';
        position: absolute;
        left: -9px;
        top: 50%;
        transform: translateY(-50%);
        height: $size;
        width: $size;
        background: $color-2;
        border-radius: 100%;
      }

      &-content {
        padding: 12px 23.5px;
        width: 100%;

        h3 {
          text-align: left;
          font-family: $font-2;
          font-weight: $weight-font-bold;
          color: $color-1;
          font-size: 18px;
          margin: 0 0 4px 0;
        }

        p {
          margin: 0;
          text-align: left;
          font-family: $font-2;
          color: $color-3;
          font-weight: $weight-font-light;
          font-size: 18px;
          line-height: 1.5;
        }
      }
    }
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
