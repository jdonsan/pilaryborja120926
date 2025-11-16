<template>
  <div id="app">
    <div v-if="!start" class="my-loading-page">
      <my-loading v-if="loading" />
      <div class="my-loading-content" v-else>
        <img class="my-loading-icon" src="@/assets/img/icon.png" alt="Icon" />
        <p>Nuestro "para Siempre" comienza</p>
        <button @click="start = true">Aquí</button>
      </div>
    </div>
    <div class="my-content">
      <my-cover />
      <my-countdown />
      <my-place />
      <my-day />
      <my-details />
      <my-form />
      <my-present />
      <my-album />
      <my-phone />
      <my-name />
      <my-footer />
      <my-music v-if="start" />
      <my-refresh v-if="updateExists" @refresh="refreshApp" />
    </div>
  </div>
</template>

<script>
import updateMixin from './mixins/update'
import MyCover from './components/MyCover/MyCover'
import MyCountdown from './components/MyCountdown/MyCountdown'
import MyLoading from './components/MyLoading/MyLoading'
import MyPlace from './components/MyPlace/MyPlace'
import MyDay from './components/MyDay/MyDay'
import MyDetails from './components/MyDetails/MyDetails'
import MyPresent from './components/MyPresent/MyPresent'
import MyForm from './components/MyForm/MyForm'
import MyAlbum from './components/MyAlbum/ MyAlbum'
import MyPhone from './components/MyPhone/MyPhone'
import MyName from './components/MyName/MyName'
import MyFooter from './components/MyFooter/MyFooter'
import MyMusic from './components/MyMusic/MyMusic'
import MyRefresh from './components/MyRefresh/MyRefresh'

export default {
  name: 'App',

  mixins: [updateMixin],

  components: {
    MyCover,
    MyCountdown,
    MyLoading,
    MyPlace,
    MyDay,
    MyDetails,
    MyPresent,
    MyForm,
    MyAlbum,
    MyPhone,
    MyName,
    MyFooter,
    MyMusic,
    MyRefresh
  },

  data() {
    return {
      start: false,
      loading: true
    }
  },

  mounted() {
    setTimeout(() => (this.loading = false), 4000)
  }
}
</script>

<style lang="scss">
body,
html {
  padding: 0;
  margin: 0;
  width: 100%;
  background: $color-5;

  div,
  section,
  article {
    box-sizing: border-box;
  }
}

h2 {
  font-family: $font-1;
  font-weight: $weight-font-bold;
  color: $color-1;
  width: 100%;
  font-size: 45px;
  line-height: 45px;
  padding: 0 15px;
  margin-bottom: 0;
  text-align: center;
  width: 100%;
}

p {
  font-family: $font-2;
  font-weight: $weight-font-regular;
  color: $color-1;
  width: 100%;
  font-size: 20px;
  line-height: 1.3;
  margin: 1rem 0;
}

h3 {
  font-family: $font-2;
  text-align: center;
  font-size: 20px;
  color: $color-2;
}

img {
  width: 100%;
  margin: 1rem 0;
}

button {
  min-width: 200px;
  border: 0;
  display: inline-block;
  background: $color-2;
  color: $color-5 !important;
  font-family: $font-2;
  font-weight: $weight-font-regular;
  padding: 1rem;
  border-radius: 5rem;
  margin: 0.5rem;
  text-decoration: none;
}

b {
  color: $color-1;
  font-weight: bold;
}

#app {
  .my-loading-page {
    background: $color-1;
    height: 100vh;
    width: 100vw;
    position: fixed;
    opacity: 0.95;
    z-index: 10000;
    @include flex-center();
  }

  .my-loading-icon {
    width: 120px;
    margin: 0 auto;
  }

  .my-loading-content {
    display: flex;
    flex-direction: column;
    align-items: center;
    justify-content: center;
    text-align: center;

    p {
      font-size: 36px;
      line-height: 36px;
      font-family: $font-2;
      font-weight: $weight-font-medium;
      color: $color-5;
      display: inline-block;
      width: 100%;
    }
  }

  .my-content {
    max-width: 768px;
    margin: 0 auto;
  }
}
</style>
