<template>
  <div id="app">
    <Header/>
    <Profiles v-bind:dinosArray="dinos" />
    <Footer/>
  </div>
</template>

<script>
import Header from './components/Header'
import Profiles from './components/Profiles'
import Footer from './components/Footer'

export default {
  name: 'App',
  components: {
    Header,
    Profiles,
    Footer
  },
  data() {
    return {
      dinos: [],
      apiURL: "https://dino2-server.herokuapp.com/"
    }
  },
  created() {
    fetch(this.apiURL)
      .then(response => {return response.json()})
      .then((json) => {
        this.dinos = json.dinosaurs;
      })

    }  
}
</script>

<style>
#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
/* 
main {
  grid-row: 2/3;
}

main section {
  padding: 0 20px 0 20px;
  display: grid;
  grid-template-columns: repeat(auto-fit, x100%);
  grid-gap: 10px;
  margin: 0 auto;
  width: 50%;
}

small {
  color: black;
  font-size: .5rem;
  margin-left: 10px;
}

p {
  font-size: .8rem;
} 
*/

</style>
