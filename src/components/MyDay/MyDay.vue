<template>
  <section class="my-day">
    <div class="my-day-rings">
      <img src="@/assets/img/rings.svg" alt="Anillos" />
    </div>

    <div class="my-day-content">
      <h2>El Gran Día</h2>

      <ul class="my-day-planning">
        <li 
          class="my-day-planning-item"
          v-for="(item, index) in planning"
          :key="index"
        >
          <div class="my-day-planning-item-picture">
            <img :src="getIcon(item.img)" :alt="item.title" />
          </div>
          <div class="my-day-planning-item-content">
            <p>{{ item.time }}</p>
            <h3>{{ item.title }}</h3>
          </div>
        </li>
      </ul>
    </div>
  </section>
</template>

<script>
export default {
  name: 'MyDay',

  data() {
    return {
      planning: [
        { 
          img: 'icon-1.svg',
          time: '17:00 PM',
          title: 'Ceremonia'
        },
        {
          img: 'icon-2.png',
          time: '18:30 PM',
          title: 'Cóctel'
        },
        {
          img: 'icon-3.png',
          time: '20:00 PM',
          title: 'Banquete'
        },
        {
          img: 'icon-4.png',
          time: '22:00 PM',
          title: 'Fiesta'
        },
        {
          img: 'icon-5.png',
          time: '00:00 PM',
          title: 'Fin (Salida Autobús)'
        }
      ]
    }
  },

  methods: {
    getIcon(name) {
      return require(`@/assets/img/my-day/${name}`)
    }
  }
}
</script>

<style lang="scss" scoped>
.my-day {
  text-align: center;
  padding-bottom: 48px;

  &-rings {
    background: url('@/assets/img/curva-5.svg') center center no-repeat;
    position: relative;
    height: 200px;
    margin-bottom: 32px;

    img {
      width: 200px;
      height: 200px;
      position: absolute;
      left: 50%;
      transform: translateX(-50%);
    }
  }

  &-planning {
    display: inline-block;

    &-item {
      display: flex;
      align-items: center;
      
      &-picture {
        padding: 16px 24px;
        border-right: 3px solid $color-2;
        position: relative;
        height: 100%;
        $size: 16px;

        &::before {
          content: '';
          position: absolute;
          right: -9px;
          top: 50%;
          transform: translateY(-50%);
          height: $size;
          width: $size;
          background: $color-2;
          border-radius: 100%;
        }

        img {
          width: 64px;
          height: 64px;
          object-fit: contain;
        }
      }

      &-content {
        padding: 23.5px;
        width: 100%;
        
        h3 {
          text-align: left;
          font-family: $font-2;
          font-weight: $weight-font-bold;
          color: $color-1;
          font-size: 18px;
          text-transform: uppercase;
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
}
</style>
