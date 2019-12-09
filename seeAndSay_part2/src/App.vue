<template>
  <div id="app">
    <Heading :heading="heading"/>
    <Tiles :tiles="tiles" :history="history" @playAudio="playAudio"/>
    <History :history="history" :tiles="tiles"/>
    <Credits :credits="credits"/>
    <audio id="audio"
        controls
        src="">
            Your browser does not support the
            <code>audio</code> element.
    </audio>
    <div>
      <img class="hide" alt="Vue logo" src="./assets/svg/a.svg">
      <img class="hide" alt="Vue logo" src="./assets/svg/e.svg">
      <img class="hide" alt="Vue logo" src="./assets/svg/i.svg">
      <img class="hide" alt="Vue logo" src="./assets/svg/o.svg">
      <img class="hide" alt="Vue logo" src="./assets/svg/u.svg">
      <img class="hide" alt="Vue logo" src="./assets/svg/ou.svg">
      <img class="hide" alt="Vue logo" src="./assets/svg/au.svg">
      <img class="hide" alt="Vue logo" src="./assets/svg/ao.svg">
      <img class="hide" alt="Vue logo" src="./assets/svg/ai.svg">
      <img class="hide" alt="Vue logo" src="./assets/svg/oi.svg">

      <img id="header" src="./assets/svg/header.svg" alt="">
    </div>
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
        {name:"Font",  list:["Work Sans","Google Fonts"]},
        {name:"Illustrations",  list:["Ravish"]},
        {name:"Audio",  list:["Text to Speech : http://www.fromtexttospeech.com/"]},
      ],
      history:[],
      tiles:[
        {letter:"a",  audio:"http://www.fromtexttospeech.com/output/0559467001575922969/52324930.mp3",img:"./assets/svg/a.svg"},
        {letter:"e",  audio:"http://www.fromtexttospeech.com/output/0452977001575924672/52325326.mp3",img:"/assets/e.svg"},
        {letter:"i",  audio:"http://www.fromtexttospeech.com/output/0831004001575924710/52325345.mp3",img:"/assets/i.svg"},
        {letter:"o",  audio:"http://www.fromtexttospeech.com/output/0648633001575924748/52325356.mp3",img:"/assets/o.svg"},
        {letter:"u",  audio:"http://www.fromtexttospeech.com/output/0881159001575924767/52325362.mp3",img:"/assets/u.svg"},
        {letter:"ou", audio:"http://www.fromtexttospeech.com/output/0787264001575925171/52325485.mp3",img:"/assets/a.svg"},
        {letter:"au", audio:"http://www.fromtexttospeech.com/output/0842025001575925255/52325505.mp3",img:"/assets/a.svg"},
        {letter:"ao", audio:"http://www.fromtexttospeech.com/output/0541656001575925308/52325525.mp3",img:"/assets/a.svg"},
        {letter:"ai", audio:"http://www.fromtexttospeech.com/output/0200665001575925489/52325596.mp3",img:"/assets/a.svg"},
        {letter:"oi", audio:"http://www.fromtexttospeech.com/output/0800631001575929404/52326528.mp3",img:"/assets/a.svg"}
        ],
    }
  },
  methods: {
    playAudio(index){
        document.getElementById("audio").src=this.tiles[index].audio;
        document.getElementById("audio").play();
        }
  },
  
mounted(){
    //this.playAudio(0);
  }
}

</script>

<style>
body{
  margin: 0px;
  font-size: 1.3rem;
  background-image: url('https://images-na.ssl-images-amazon.com/images/I/512%2BQ5DwnSL._SX466_.jpg');
  background-color: #f7e8dc
}
.hide,#header{
  display:none;
}
#audio
{
  display: none
}
#app {
  font-family: 'Work Sans','Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
}

</style>
