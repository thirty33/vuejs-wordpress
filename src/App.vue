<template>
  <div id="my-app" class="page-wrapper">
    
    <app-encabezado></app-encabezado>
    <middle></middle>
    <b-container>
      <div class="subtitle text-center">
        <h2>LINEA DE EQUIPOS EN ACERO INOXIDABLE</h2>
      </div>
    </b-container>
    <equipos></equipos>


    
  </div>
</template>

<script>
import { mapGetters, mapActions, mapMutations } from 'vuex'
import Encabezado from './components/partials/Encabezado'
import Middle from './components/partials/Middle'
import Equipos from './components/partials/Equipos'


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
  // @import './styles/app.scss';
  body {
    // background: linear-gradient(to right, #B9B9B9, white); 
    background: linear-gradient(90deg, #B9B9B9, white); 
  }

  .subtitle {
    padding: 80px 0; 
  }
</style>
