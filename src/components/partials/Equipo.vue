<template>
  <div class="equipo">
        <b-card title=""
                :img-src="this.data.img"
                img-alt="Image"
                img-top
                tag="article"
                style="max-width: inherit;"
                class="mb-2 equipo_card"
                :height="this.data.dim"
                >
            <h3>{{this.data.name}}</h3>
            <h4>{{this.data.type}}</h4>
            <p class="card-text">
            Dimensiones externas (mm)
            </p>
            <ul class="equipo_card_ul">
              <li>Alto: {{this.data.height}}</li>
              <li>Ancho: {{this.data.width}}</li>
              <li>Prof: {{this.data.prof}}</li>
            </ul>
        </b-card>
    </div>
</template>

<script>
export default {
  props: ['data'],
  data () {
      return {

      }
  }
}
</script>

<style lang="scss">
  .equipo {
    // background-color: #ACACAC;
    margin: 0 0;
    &_card {
      background-color: transparent;
      margin: 0 0;
      border: 0 0;
      border: none !important;

      p {
        margin-bottom: 0;
      }
      &_ul {
        list-style: none;
        

        li {
          padding-left: 78px;
        }
      }
    }
    
  }

  .card-body {
    padding: 0 0 !important;
    border-right: 1px solid #9D9D9D;

    h4 {
      border-bottom: 1px solid #9D9D9D;
      padding-bottom: 16px;
    }
  }

</style>


