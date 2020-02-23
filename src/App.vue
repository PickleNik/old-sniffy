<template>
  <v-app>
  <v-layout row class="pa-3 hidden-md-and-up width white round2" style="z-index: 10;box-shadow: 0 0 10em 5em white;position: fixed; top: 0; left: 0;">
    <v-avatar size="50">
       <img src="./assets/sniff-ios.svg"/>
    </v-avatar>
    <span class="amber--text" style="font-size: 3em;  font-weight: 900;">Sniffy</span>
  </v-layout>
  <v-layout row class="pa-3 hidden-sm-and-down white round2" style="z-index: 10;box-shadow: 0 0 10em 5em white;position: fixed; top: 0; left: 0;">
    <v-avatar size="70">
       <img src="./assets/sniff-ios.svg"/>
    </v-avatar>
    <span class="amber--text" style="font-size: 4em;  font-weight: 900;">Sniffy</span>
  </v-layout>
  <v-flex xs12 class="height">
    <vue-particles style="width:100vw;height:100vh;"
    color="#FFC107" class="hidden-xs-only"
    :particleOpacity="0.5"
    :particlesNumber="50"
    shapeType="circle"
    :particleSize="5"
    linesColor="#E91E63"
    :linesWidth="1"
    :lineLinked="true"
    :lineOpacity="0.5"
    :linesDistance="150"
    :moveSpeed="3"
    :hoverEffect="true"
    hoverMode="grab"
    :clickEffect="true"
    clickMode="repulse"
    ></vue-particles>
    <v-flex xs12 sm12 md12 lg8 offset-lg2 class="white" style="z-index: 1;box-shadow: 0 0 10em 5em white; border-radius: 3em; position: absolute; top: 50vh; transform: translateY(-50%);">
      <v-layout row wrap>
        <v-flex class="mr-3 hidden-md-and-down">
          <v-img class="round2" style="height: 44vh;" contain src="untitled (1).png"></v-img>
        </v-flex>
        <v-flex xs12 sm10 offset-sm1 md6 class="pa-3 mx-auto">
          <span class="gradient-text" style="font-size: 4em;  font-weight: 900; text-shadow: 0 0 1em #E91E6366"><span id="good" class="gradient--text"></span> Good</span>
          <p class="grey--text" style="font-size: 2em; text-align: justify;">Find a perfect perfume with a help of Neural Network. Let our algorithm choose the perfume that matches you based on your reviews.</p>
          <v-layout row wrap>
            <v-flex xs6>
              <v-text-field solo color="pink" clearable type="email" placeholder="Email" class="mt-3" prepend-inner-icon="alternate_email"></v-text-field>
            </v-flex>
            <v-flex xs6>
              <v-btn dark large style="font-weight: 600; height: 48px !important; border-top-right-radius: 2em; border-bottom-right-radius: 2em;" class="mt-3" color="pink">Subscribe</v-btn>
            </v-flex>
          </v-layout>
          <v-radio-group v-model="radioGroup">
            <v-layout row>
              <v-radio color="pink" class="my-auto ml-4" style="margin-top: -1em !important;"
              v-for="n in 2"
              :key="n"
              :label="labels[n]"
              :value="n"
              ></v-radio>
            </v-layout>
          </v-radio-group>
        </v-flex>
        </v-layout>
    </v-flex>
  </v-flex>
  <v-flex xs12 sm12 md8 offset-md2 class="height">
    <v-layout column>
      <span class="gradient-text mx-auto my-5" style="font-size: 4em;  font-weight: 900; text-shadow: 0 0 1em #E91E6366">Probes</span>
      <p class="mt-3 mx-3 grey--text" style="font-size: 2em; text-align: justify;">Get free probes and leave reveiws to personalize our Neural Net. Receive rewards for participating in surveys!</p>
      <v-layout row wrap>
        <v-flex v-for="n in 9" :key="n" class="ma-3 elevation-10">
          <v-layout>
            <v-avatar tile size="70"><img src="./assets/sniff-ios.svg"/></v-avatar>
            <h2 class="my-auto" style="font-size:2.5em;"># {{ 10 + n }}</h2>
            <v-spacer></v-spacer>
            <v-icon large class="amber--text">star</v-icon>
            <v-icon large class="gradient-text">star_half</v-icon>
            <v-icon large class="pink--text mr-3">star_outline</v-icon>
          </v-layout>
        </v-flex>
      </v-layout>
    </v-layout>
  </v-flex>
  <v-flex xs12 sm10 offset-sm1 md8 offset-md2>
    <span lass="my-3 mx-auto grey--text" style="font-size: 2em;">Made with 💖 by Smart Scent Group © 2019.</span>
  </v-flex>
  </v-app>
</template>

<script>
import Typed from 'typed.js'

export default {
  data () {
    return {
      radioGroup: null,
      labels: ['error', 'I am a partner', 'I am a user'],
      titles: ['Smell', 'Feel']
    }
  },
  mounted () {
    // eslint-disable-next-line
    new Typed('#good', {
      strings: this.titles,
      loop: true,
      typeSpeed: 100,
      backSpeed: 11,
      startDelay: 0,
      backDelay: 3000,
      smartBackspace: true,
      showCursor: false
    })
  }
}
</script>

<style>
@import url('https://fonts.googleapis.com/css?family=Montserrat:400,600,900');
* {
  font-family: 'Montserrat'; color: #444;
}
@media only screen and (max-width: 960px) {
  /* h1 {
    font-size: 0.9em !important;
  }
  p {
    font-size: 1.5em !important;
  }
  span {
    font-size: 3em !important;
  } */
  /* .gradient-text {
    font-size: 0.5em !important;
  } */
}
::-webkit-scrollbar{
  width: 0;
}
.height {
  height: 100vh !important;
}
.width {
  width: 100vw;
}
.round1 {
  border-radius: 1em;
}
.round2 {
  border-radius: 2em;
}
.gradient-text{
  background: linear-gradient(120deg, #fec035 0%, rgba(255,162,0,1) 50%, rgba(233,30,99,1) 100%);
  -webkit-background-clip: text;
  -webkit-text-fill-color: transparent;
}
.v-input__slot{
  border-top-left-radius: 2em !important;
  border-bottom-left-radius: 2em !important;
  border-color: #E91E63 !important;
}
.hover{
  opacity: 0;
  transition-duration: 0.5s;
  transition-timing-function: ease;
  transition-property: all;
}
.hover:hover{
  opacity: 1;
}
.link {
  text-decoration: none;
  position: relative;
}
/* Kukuri */
.link--kukuri {
  text-transform: uppercase;
  font-weight: 900;
  overflow: hidden;
  line-height: 0.75;
}

.link--kukuri:hover {
  color: #E91E63 !important;
}

.link--kukuri::after {
  content: '';
  position: absolute;
  height: 6px;
  width: 100%;
  top: 50%;
  margin-top: -4px;
  right: 0;
  background: #E91E63 !important;
  border-radius:1em;
  -webkit-transform: translate3d(-111%,0,0);
  transform: translate3d(-111%,0,0);
  -webkit-transition: -webkit-transform 0.4s;
  transition: transform .3s;
  -webkit-transition-timing-function: cubic-bezier(0.7,0,0.3,1);
  transition-timing-function: cubic-bezier(0.7,0,0.3,1);
}

.link--kukuri:hover::after {
  -webkit-transform: translate3d(100%,0,0);
  transform: translate3d(100%,0,0);
}
.link--kukuri:hover::before {
  width: 100%;
}
.scale {
  transition-duration: 0.5s;
  transition-timing-function: ease-in-out;
  transition-property: all;
}
.scale:hover {
  transform: scale(1.1);
}
</style>
