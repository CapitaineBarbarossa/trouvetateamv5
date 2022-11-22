<template>
  <div class="home">
    <!--<img alt="Vue logo" src="../assets/logo.png">-->
    <Carousel />
    <div class="container marketing">    
        <div class="row">
            <Detail v-for="(detail,index) in details" :key="index" :id="detail.id" :titre="detail.titre" :image="detail.image"  />
        </div>
    </div>
  </div>
</template>

<script>
// @ is an alias to /src
import Carousel from '@/components/Carousel.vue'
import axios from 'axios'

export default {
  name: 'Accueil',
  components: {
    Carousel,
  },
  /*data(){
        return {
            details:[
                {
                  titre:'Gîte',
                  image:'gite.png',
                },
                {
                  titre:'Randonnée',
                  image:'randonnee.png',
                },
                {
                  titre:'Ski',
                  image:'ski.png',
                },
            ],
        }
    },*/
  data(){
        return {
            details:[],
            errors: []
        }
  },
  // Fetches Details when the component is created.
  created() {
    // axios.get(`https://localhost:8000/api/details.jsonld`)
    // axios.get(`https://localhost:8000/api/details`)    
    // axios.get(`http://localhost:8081/details2.json`)
    axios.get(`http://localhost:8080/games.json`)
    .then(response => {
      // JSON responses are automatically parsed.
      // this.details = response.data['hydra:member'] // fonctionne avec l'api
      this.games = response.data.games
    })
    .catch(e => {
      this.errors.push(e)
    })
  }  
}
</script>