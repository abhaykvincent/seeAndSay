<template>
  <div id="app">
    <Heading :heading="heading"/>
    <Tiles :tiles="tiles" :history="history"/>
    <History :history="history"/>
    <Credits :credits="credits"/>
  </div>
</template>

<script>
import Heading from './components/Heading.vue'
import Tiles from './components/Tiles.vue'
import History from './components/History.vue'
import Credits from './components/Credits.vue'

export default {
  name: 'app',
  components: {
    Heading,
    Tiles,
    History,
    Credits
  },
  data() {
    return {
      showCompletion: "",
      heading:"Vowel Learner",
      credits:[
        {name:"Group Members",  list:["Aarsh","Ravish","Abhay"]},
        {name:"Font",  list:["Google Fonts"]}
      ],
      history:[],
      tiles:['a','e','i','o','u','aa','ee','ii','oo','uu']
    }
  }
}
</script>

<style>
body{
  margin: 0px;
  font-size: 1.3rem;
}
#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
}

</style>
