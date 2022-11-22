<template>
  <Header/>

    <router-view/>

  <Footer/>
</template>

<script>
// @ is an alias to /src
import Header from '@/components/Header.vue'
import Footer from '@/components/Footer.vue'


export default {
  components: {
    Header,
    Footer,
  },
  data() {
    return {
    }
  },
  methods: {
    
  }
}
</script>