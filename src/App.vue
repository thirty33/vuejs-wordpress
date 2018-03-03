<template>
  <div id="my-app" class="page-wrapper">
    <!-- <transition
      name="loader-animation"
      enter-active-class="animated fadeIn"
      leave-active-class="animated fadeOut">
      <div class="progress loader" v-if="showLoader">
        <div class="progress-bar" role="progressbar" :style="loaderStyle" aria-valuenow="100" aria-valuemin="0" aria-valuemax="100"></div>
      </div>
    </transition> -->

    <!-- <app-header></app-header> -->
    <app-encabezado></app-encabezado>
    <middle></middle>
    <b-container>
      <div class="subtitle">
        <h2>LINEA DE EQUIPOS EN ACERO INOXIDABLE</h2>
      </div>
    </b-container>
    <equipos></equipos>


    <!-- <transition name="page-transition" mode="out-in" appear>
      <div class="page-content-wrapper">
        <router-view></router-view>
      </div>
    </transition> -->

    <!-- <app-footer></app-footer> -->
  </div>
</template>

<script>
import { mapGetters, mapActions, mapMutations } from 'vuex'
import Header from './components/partials/Header'
import Encabezado from './components/partials/Encabezado'
import Middle from './components/partials/Middle'
import Equipos from './components/partials/Equipos'
import Footer from './components/partials/Footer'

export default {
  data() {
    return {
      showLoader: true
    }
  },
  computed: {
    ...mapGetters({
      isLoading: 'isLoading',
      loadingProgress: 'loadingProgress'
    }),

    loaderStyle() {
      return `width: ${this.loadingProgress}%;`
    }
  },

  components: {
    appHeader: Header,
    appFooter: Footer,
    appEncabezado: Encabezado,
    middle: Middle,
    equipos: Equipos
  },

  watch: {
    // watch the value of isLoading and once it's false hide the loader
    isLoading(val) {
      if (val == false) {
        let self = this
        setTimeout(function(){
          self.showLoader = false
        }, 1000)
      }
    }
  }
}
</script>
<style lang="scss">
  @import './styles/app.scss';
</style>
