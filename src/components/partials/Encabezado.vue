<template>
    <b-container class="container">
        <b-row class="container_fila1">
            <b-col md="4" class="container_fila1_col1">
              <b-img center src="https://firebasestorage.googleapis.com/v0/b/jetsetdatabase.appspot.com/o/logo%20imbera.png?alt=media&token=b631cf8e-5136-4c1f-904b-c3682d387c41" fluid alt="Responsive image" />
            </b-col>
            <b-col md="3" class="container_fila1_col2">
              <b-img src="https://firebasestorage.googleapis.com/v0/b/jetsetdatabase.appspot.com/o/chef%20(1).png?alt=media&token=d52f9540-e8d7-4a47-ae2f-6282e6533a6e" fluid alt="Responsive image" />
            </b-col>
            <b-col md="5" class="container_fila1_col3">
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
      }
      &_col1 {
        
      }
      &_col3 {
      
      }
    }
  }

</style>


