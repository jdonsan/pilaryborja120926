<template>
  <section class="my-countdown">
    <div class="my-countdown-container">
      <div class="my-countdown-content">
        <img
          class="my-countdown-picture"
          src="@/assets/img/contador-flores.webp"
          alt="contador"
        />
        <h3>Faltan</h3>

        <div class="my-countdown-clock">
          <div class="my-countdown-clock-col">
            <span class="number">{{ days }}</span>
            <span class="time">DÍAS</span>
          </div>

          <div class="my-countdown-clock-col">
            <span class="number">{{ hours }}</span>
            <span class="time">HS</span>
          </div>

          <div class="my-countdown-clock-col">
            <span class="number">{{ minutes }}</span>
            <span class="time">MIN</span>
          </div>

          <div class="my-countdown-clock-col">
            <span class="number">{{ seconds }}</span>
            <span class="time">SEG</span>
          </div>
        </div>
      </div>
    </div>
  </section>
</template>

<script>
export default {
  name: 'MyCountdownContainer',

  data() {
    return {
      isToday: false,
      days: 0,
      hours: 0,
      minutes: 0,
      seconds: 0
    }
  },

  mounted() {
    this.run()
  },

  methods: {
    run() {
      const countDownDate = new Date('September 12, 2026 01:00:00').getTime()
      const interval = setInterval(() => {
        const now = new Date().getTime()
        const distance = countDownDate - now

        this.days = Math.floor(distance / (1000 * 60 * 60 * 24))
        this.hours = Math.floor(
          (distance % (1000 * 60 * 60 * 24)) / (1000 * 60 * 60)
        )
        this.minutes = Math.floor((distance % (1000 * 60 * 60)) / (1000 * 60))
        this.seconds = Math.floor((distance % (1000 * 60)) / 1000)

        if (distance < 0) {
          clearInterval(interval)
          this.isToday = true
        }
      }, 1000)
    }
  }
}
</script>

<style lang="scss" scoped>
.my-countdown {
  background: $color-5;

  &-container {
    margin: 0 auto;
    background: $color-5;
    height: 340px;
  }

  &-picture {
    position: absolute;
    width: 170px;
    top: -40px;
    left: -10px;
  }

  &-content {
    position: relative;
    background: url('@/assets/img/contador.svg') center center no-repeat;
    background-size: contain;
    z-index: 1000;
    width: 100%;
    max-width: 320px;
    max-height: 320px;
    min-width: 320px;
    min-height: 320px;
    margin: 0 auto;
    @include flex-center();
    flex-direction: column;

    h3 {
      font-family: $font-1;
      font-weight: $weight-font-bold;
      color: $color-1;
      width: 100%;
      text-align: center;
      font-size: 45px;
    }
  }

  &-clock {
    font-family: $font-2;
    display: flex;
    margin: 1rem 0;

    &-col {
      padding: 0 8px;
      border-right: 1px solid #ccc;

      &:last-child {
        border-right: 0px;
      }

      span {
        display: block;
        text-align: center;
      }

      .number {
        font-size: 35px;
        font-weight: $weight-font-medium;
        font-family: $font-2;
        color: $color-1;
        margin-bottom: 0.5rem;
      }

      .time {
        font-size: 18px;
        font-weight: $weight-font-light;
        font-family: $font-2;
        color: $color-3;
      }
    }
  }
}
</style>
