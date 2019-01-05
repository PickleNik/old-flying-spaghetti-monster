<template>
  <v-app dark class="head">
    <v-container fluid class="app">
      <v-flex md3 lg2 class="inDown hidden-sm-and-down pa-4" style="position:fixed; z-index: 100; left:0; top:0;">
        <v-layout column>
          <v-layout row class="mb-3" ><v-icon left color="amber">fas fa-pastafarianism</v-icon><h3>Pastafarianism</h3> </v-layout>
          <a href="https://www.venganza.org/about/" target="_blank"><v-btn small round flat class="mx-0 link link--kukuri"><v-icon left class="amber--text">web</v-icon>Official Website</v-btn></a>
          <a href="https://en.wikipedia.org/wiki/Flying_Spaghetti_Monster" target="_blank"><v-btn small round flat class="mx-0 link link--kukuri"><v-icon left class="amber--text">fas fa-globe</v-icon>Wikipedia</v-btn></a>
          <a href="https://www.youtube.com/watch?v=7sfnnJBk3aY" target="_blank"><v-btn small round flat class="mx-0 link link--kukuri"><v-icon left class="amber--text">fab fa-youtube</v-icon>Youtube</v-btn></a>
        </v-layout>
      </v-flex>
      <v-flex md3 lg2 class="inDown hidden-sm-and-down pa-4" style="position:fixed; z-index: 100; right:0; top:0;">
        <h3>352,198,078<v-icon right color="amber">group</v-icon></h3>
      </v-flex>
      <b class="pt-3 mr-3 inUp" style="position:fixed; z-index: 100; right:0; bottom:0;" id="info">Made with <s class="pink">love</s> a <span class="purple">keyboard</span> by
        <v-avatar size="40" class="mx-2 mb-3">
          <img src="./assets/me.jpg">
        </v-avatar>
        <a href="https://nikita-krupin.firebaseapp.com">
          <v-btn small round flat class="ma-0 px-0 link link--kukuri">
            PickleNik
          </v-btn>
        </a>
      </b>
      <v-layout row wrap>
        <v-flex xs12 sm12 md6 offset-md3 lg8 offset-lg2 class="text-xs-center mb-5">
          <v-layout column>
            <card3d id="face" class="zoom mx-auto my-3 hidden-xs-only" style="border-radius:100%; width:20em; height:20em;" data-image="https://i.pinimg.com/originals/88/24/27/8824273c0361aea1d755112a05bdbca0.gif">
              <span slot="header" class="amber--text" style="font-family: 'Permanent Marker'; font-size: 1.5em;">Flying Spaghetti Monster</span>
              <p slot="content" style="text-align: justify;" class="px-3 my-5"> <b>" I'd Really Rather You Didn't Use My Existence As A Means To Oppress, Subjugate, Punish, Eviscerate, And/Or, You Know, Be Mean To Others. I Don't Require Sacrifices, And Purity Is For Drinking Water, Not People."</b></p>
            </card3d>
            <img id="face" class="mx-auto my-3 hidden-sm-and-up" src="https://i.pinimg.com/originals/88/24/27/8824273c0361aea1d755112a05bdbca0.gif">
            <p class="pt-2 mb-3 pb-3 text-xs-justify" style="font-size: 1.5em; min-height: 4.5em; font-family: 'Roboto Mono'" id="greeting"></p>
          </v-layout>
        </v-flex>
      </v-layout>
    </v-container>
  </v-app>
</template>

<script>
import card3d from './components/3d.vue'
import Typed from 'typed.js'

export default {
  components: {
    card3d: card3d
  },
  data () {
    return {
      typedOptions: [
        'Hello there',
        '&nbsp;&nbsp;&nbsp;&nbsp;Pastafarianism (a portmanteau of pasta and Rastafarianism) is a social movement that promotes a light-hearted view of religion and opposes the teaching of intelligent design and creationism in public schools. According to adherents, Pastafarianism is a "real, legitimate religion, as much as any other". <br/><br/> &nbsp;&nbsp;&nbsp;&nbsp;The Flying Spaghetti Monster (FSM) is the deity of the Church of the Flying Spaghetti Monster, or Pastafarianism. Pastafarianism (a portmanteau of pasta and Rastafarianism) is a social movement that promotes a light-hearted view of religion and opposes the teaching of intelligent design and creationism in public schools. According to adherents, Pastafarianism is a "real, legitimate religion, as much as any other". In New Zealand, Pastafarian representatives are authorized to officiate weddings. However, in the United States, a federal judge has ruled that the "Church of the Flying Spaghetti Monster" is not a real religion. In August 2018 the Dutch Council of State also ruled that Pastafarianism is not a religion. <br/><br/> &nbsp;&nbsp;&nbsp;&nbsp;The "Flying Spaghetti Monster" was first described in a satirical open letter written by Bobby Henderson in 2005 to protest the Kansas State Board of Education decision to permit teaching intelligent design as an alternative to evolution in public school science classes. In the letter, Henderson demanded equal time in science classrooms for "Flying Spaghetti Monsterism", alongside intelligent design and evolution. After Henderson published the letter on his website, the Flying Spaghetti Monster rapidly became an Internet phenomenon and a symbol of opposition to the teaching of intelligent design in public schools. <br/><br/> &nbsp;&nbsp;&nbsp;&nbsp;Pastafarian tenets (generally satires of creationism) are presented both on Henderson\'s Church of the Flying Spaghetti Monster website, where he is described as "prophet", and in The Gospel of the Flying Spaghetti Monster, written by Henderson in 2006. The central belief is that an invisible and undetectable Flying Spaghetti Monster created the universe. Pirates are revered as the original Pastafarians. Henderson asserts that a decline in the number of pirates over the years is the cause of global warming. The FSM community congregates at Henderson\'s website to share ideas about the Flying Spaghetti Monster and crafts representing images of it. <br/><br/> &nbsp;&nbsp;&nbsp;&nbsp;Because of its popularity and exposure, the Flying Spaghetti Monster is often used as a contemporary version of Russell\'s teapot—an argument that the philosophic burden of proof lies upon those who make unfalsifiable claims, not on those who reject them. Pastafarianism has received praise from the scientific community and criticism from proponents of intelligent design. Pastafarians have engaged in disputes with creationists, including in Polk County, Florida, where they played a role in dissuading the local school board from adopting new rules on teaching evolution.'
      ]
    }
  },
  mounted () {
    new Typed('#greeting', {// eslint-disable-line no-new
      strings: this.typedOptions,
      loop: false,
      typeSpeed: 30,
      backSpeed: 10,
      startDelay: 3000,
      backDelay: 2000,
      smartBackspace: true,
      showCursor: false
    })
  }
}
</script>

<style media="screen">
@import url('https://fonts.googleapis.com/css?family=Roboto+Mono');
@import url('https://fonts.googleapis.com/css?family=Permanent+Marker');
@import url('https://fonts.googleapis.com/css?family=Quicksand');
*{
  font-family: 'Quicksand', sans-serif;
}
html{
  background: black;
}
a {
  text-decoration: none !important;
}
body{
  overflow-y: scroll;
  -webkit-overflow-scrolling: touch;
}
.head{
  position: relative;
}
.head::before{
  content: "";
  top: 0;
  left: 0;
  width: 100%;
  height: 100%;
  position: absolute;
  background-image: url('https://upload.wikimedia.org/wikipedia/commons/9/90/Touched_by_His_Noodly_Appendage_HD.jpg');
  background-position: center center;
  background-size: cover;
  background-attachment: fixed;
  background-repeat: no-repeat;
  filter: brightness(50%);
}
::-webkit-scrollbar{
  width: 0;
}
::selection{
  background:transparent;
  color: amber;
}
@keyframes rollIn {
  from {
    opacity: 0;
    transform: translate3d(-100%, 0, 0) rotate3d(0, 0, 1, -120deg);
  }

  to {
    opacity: 1;
    transform: none;
  }
}
@keyframes zoomIn {
  from {
    opacity: 0;
    transform: scale3d(.3, .3, .3);
  }

  50% {
    opacity: 1;
  }
  to {
    opacity: 1;
  }
}
@keyframes fadeInDown {
  from {
    opacity: 0;
    transform: translate3d(0, -100%, 0);
  }

  to {
    opacity: 1;
    transform: none;
  }
}
@keyframes fadeInUp {
  from {
    opacity: 0;
    transform: translate3d(0, 100%, 0);
  }

  to {
    opacity: 1;
    transform: none;
  }
}
#face{
  opacity: 0;
  height: 30vh;
  width: 30vh;
  border-radius: 100%;
  animation: rollIn 1s 1.5s ease 1 forwards;
}
.zoom{
  opacity:0;
  animation: zoomIn 1s 2s ease 1 forwards;
}
.inUp{
  opacity:0;
  animation: fadeInUp 1s 2s ease 1 forwards;
}
.inDown{
  opacity:0;
  animation: fadeInDown 1s 2s ease 1 forwards;
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
  color: white;
}

.link--kukuri:hover {
  color: #FFC107;
}

.link--kukuri::after {
  content: '';
  position: absolute;
  height: 6px;
  width: 100%;
  top: 50%;
  margin-top: -4px;
  right: 0;
  background: #FFC107;
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
</style>
