<template>
  <div>
        <b-card title=""
                :img-src="this.data.img"
                img-alt="Image"
                img-top
                tag="article"
                style="max-width: 15rem;"
                class="mb-2">
            <h3>{{this.data.name}}</h3>
            <h4>{{this.data.type}}</h4>
            <p class="card-text">
            Dimensiones externas (mm)
            </p>
            <ul>
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

<style>

</style>


