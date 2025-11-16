<template>
  <section class="my-phone">
    <h2>Nuestros contactos</h2>
    <p>
      Si tienes alguna duda y necesitas contactar con nosotros, estos son
      nuestros números de teléfono
    </p>

    <div class="my-phone-content">
      <article class="my-phone-contact">
        <img :src="womanImage" alt="Phone Icon" />
        <p>+34 617 91 62 89</p>
      </article>

      <article class="my-phone-contact">
        <img :src="manImage" alt="Phone Icon" />
        <p>+34 637 96 30 29</p>
      </article>
    </div>
  </section>
</template>

<script>
export default {
  name: 'MyPhone',

  data() {
    return {
      womanImageCounter: 1,
      manImageCounter: 2
    }
  },

  computed: {
    womanImage() {
      return this.getImagePath(`woman-${this.womanImageCounter}.jpg`)
    },

    manImage() {
      return this.getImagePath(`man-${this.manImageCounter}.jpg`)
    }
  },

  mounted() {
    this.setImage()
  },

  methods: {
    getImagePath(counter) {
      return require(`@/assets/img/my-phone/${counter}`)
    },

    setImage() {
      setInterval(() => {
        if (this.womanImageCounter > 3) {
          this.womanImageCounter = 1
        } else {
          this.womanImageCounter = this.womanImageCounter + 1
        }

        if (this.manImageCounter > 3) {
          this.manImageCounter = 1
        } else {
          this.manImageCounter = this.manImageCounter + 1
        }
      }, 500)
    }
  }
}
</script>

<style lang="scss" scoped>
.my-phone {
  padding: 0 16px 48px;

  &-content {
    display: flex;
    align-items: center;
    justify-content: center;
    gap: 20px;
    margin-top: 20px;
  }

  &-contact {
    display: flex;
    flex-direction: column;
    align-items: center;

    img {
      width: 138px;
      height: 138px;
      margin-bottom: 10px;
      border-radius: 100%;
      filter: grayscale(1);
    }

    p {
      font-family: $font-2;
      color: $color-1;
      font-size: 18px;
      font-weight: $weight-font-regular;
    }
  }

  h2 {
    font-family: $font-1;
    font-weight: $weight-font-bold;
    color: $color-1;
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
