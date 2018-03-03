<template>
    <b-container class="container">
        <b-row class="container_fila1">
            <b-col md="3" class="container_fila1_col1">
              <b-img center src="https://firebasestorage.googleapis.com/v0/b/jetsetdatabase.appspot.com/o/logo%20imbera.png?alt=media&token=b631cf8e-5136-4c1f-904b-c3682d387c41" fluid alt="Responsive image" />
            </b-col>
            <b-col md="4" class="container_fila1_col2">
              <b-img src="https://firebasestorage.googleapis.com/v0/b/jetsetdatabase.appspot.com/o/chef%20(1).png?alt=media&token=d52f9540-e8d7-4a47-ae2f-6282e6533a6e" fluid alt="Responsive image" />
            </b-col>
            <b-col md="5" class="container_fila1_col3 mb-3 mt-3">
              <app-form></app-form>
            </b-col>
        </b-row>
    </b-container>
</template>


<script>
import Form from './Formulario'
export default {
  components: {
    appForm: Form
  },
  data () {
      return {

      }
  }
}
</script>

<style lang="scss">

  .container {
    &_fila1 {
      // background-color: green;  

      &_col2 {
        display: flex;
        // justify-items: center;
        img {
          position: absolute;
          bottom: 0;
          left: 118px;
          z-index: 5;
        }
      }
      &_col1 {
        img {
          position: absolute;
          left: 149px;
          bottom: 0;
          top: 0;
        }
      }
      &_col3 {
        padding: 0 0;
        margin-top: 1rem !important;
      }
    }
  }

</style>


