<template>
  <b-container class="container">
      <b-row v-for="item in items" :key="item.key">
        <b-col>
          <equipo :data="item"></equipo>
        </b-col>
      </b-row>
  </b-container>
</template>

<script>
import Equipo from './Equipo'
export default {
  components: {
    equipo: Equipo
  },
  data () {
      return {
        items: [
          {img: 'https://firebasestorage.googleapis.com/v0/b/jetsetdatabase.appspot.com/o/CV15.png?alt=media&token=d170ccca-39f4-4091-ab97-8395e94867c3', name: 'CV15', type: 'congelador', height: '1794', width: '750', prof: '745'},
          {img: 'https://firebasestorage.googleapis.com/v0/b/jetsetdatabase.appspot.com/o/CV18.png?alt=media&token=22919297-0df8-415d-9b3f-8cf04ca4b8bc', name: 'CV18', type: 'congelador', height: '2060', width: '750', prof: '745'},
          {img: 'https://firebasestorage.googleapis.com/v0/b/jetsetdatabase.appspot.com/o/RV18.png?alt=media&token=d501702c-e74d-44ce-abb2-c7132b525d4e', name: 'RV18', type: 'refrigerador', height: '2060', width: '750', prof: '745'},
          {img: 'https://firebasestorage.googleapis.com/v0/b/jetsetdatabase.appspot.com/o/RV15.png?alt=media&token=b05a93c7-a532-4d69-a0dc-8069dd068e00', name: 'RV15', type: 'refrigerador', height: '1794', width: '750', prof: '745'}
        ]
      }
  }
}
</script>


<style>

</style>

