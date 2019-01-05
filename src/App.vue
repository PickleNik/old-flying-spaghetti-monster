<template>
  <v-app dark class="head">
    <v-container fluid class="app">
      <v-flex md3 lg2 class="zoom hidden-sm-and-down pa-4" style="position:fixed; z-index: 100; left:0; top:0;">
        <v-layout column>
          <h1 class="mb-3">
            <v-layout row style="font-family: 'Indie Flower', sans-serif;"><v-icon left large color="amber">fas fa-pastafarianism</v-icon>Pastafarianism</v-layout>
          </h1>
          <a v-for="nav in navs" :key="nav.name" href="#" v-scroll-to="{el: nav.href, offset: -50}">
            <v-btn small round flat class="ma-0 pr-2 link link--kukuri">
              <v-icon left class="amber--text">{{ nav.icon }}</v-icon>
              {{ nav.name }}
            </v-btn>
          </a>
        </v-layout>
      </v-flex>
      <v-flex md3 lg2 class="zoom hidden-sm-and-down pa-4" style="position:fixed; z-index: 100; right:0; top:0;">
        <h3>35,098,078<v-icon right color="amber">group</v-icon></h3>
      </v-flex>
      <b class="py-3 mr-3" style="position:fixed; z-index: 100; right:0; bottom:0;" id="info">Made with <s class="pink">love</s> a<span class="amebr--text"> keyboard </span> by
        <v-avatar size="28" class="mx-2">
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
            <img id="face" class="mx-auto my-3" src="https://i.pinimg.com/originals/88/24/27/8824273c0361aea1d755112a05bdbca0.gif">
            <p class="pt-2 text-xs-justify" style="font-size: 1.5em; min-height: 4.5em;" id="greeting"></p>
          </v-layout>
        </v-flex>
      </v-layout>
    </v-container>
  </v-app>
</template>

<script>
import Typed from 'typed.js'
// import firebase from 'firebase/app'
// import 'firebase/auth'

export default {
  data () {
    return {
      typedOptions: ['Hi there', '3,4-Methyl​enedioxy​methamphetamine(or MDMA), commonly known as ecstasy, is a psychoactive drug primarily used as a recreational drug. The desired effects include altered sensations and increased energy, empathy, and pleasure. When taken by mouth, effects begin after 30–45 minutes and last 3–6 hours.'],
      direction: 'bottom',
      posts: [
        {
          title: 'What is Molly',
          typed: true,
          fab: false,
          id: 'post1',
          links: [
            { title: 'Outline', href: 'https://docs.google.com/document/d/1iZa7Gf0W3FIoVVw-vEPF_gbyCfb3pTEAJkVRuuvI--A/edit?usp=sharing' }
          ]
        },
        {
          title: 'Quiz',
          comment: '',
          fab: false,
          id: 'post2',
          text: 'Tip of the day: Ecstasy, in fact, is a term for Molly which has been chemically altered with other additives, such as amphetamine, caffeine etc.',
          links: [
            { title: 'Quiz', href: 'https://www.justthinktwice.gov/quiz/quiz-ecstasy-and-mdma' },
            { title: 'Source 1', href: 'https://www.drugabuse.gov/publications/drugfacts/mdma-ecstasymolly' },
            { title: 'Source 2', href: 'https://teens.drugabuse.gov/drug-facts/mdma-ecstasy-or-molly' },
            { title: 'Source 3', href: 'https://abovetheinfluence.com/drugs/mdma/' }
          ]
        },
        {
          title: 'Video',
          comment: '',
          fab: false,
          id: 'post3',
          video: 'https://www.youtube.com/embed/jEAr7ThsYew'
        },
        {
          title: 'Article',
          text: 'Developed in 1914 as an appetite suppressant, MDMA gained popularity in the 1980s with young adults at large music festivals and all-night dance parties or raves. \n The user experiences feelings of euphoria, increased energy, intimacy and emotional warmth, sensitivity to touch, and a distortion of time and of the senses. \n Ecstasy is frequently taken with other illegal drugs, and pills sold as MDMA on the street often contain additives. These factors can contribute to serious, and sometimes fatal, health effects. \n MDMA can also be addictive, and research suggests that long-term cognitive problems may develop in some users.',
          comment: '',
          fab: false,
          id: 'post4',
          links: [
            { title: 'Full Article', href: 'https://www.medicalnewstoday.com/articles/297064.php' }
          ]
        },
        {
          title: 'Post 5',
          comment: '',
          image: 'https://media.giphy.com/media/pWP6AQg2KMc2Q/giphy.gif',
          fab: false,
          id: 'post5',
          video: 'https://www.youtube.com/embed/_sXhbieSzZs'
        }
      ],
      navs: [
        { name: 'Creator', href: '#title', icon: 'assignment_ind' },
        { name: 'About', href: '#post1', icon: 'assignment' },
        { name: 'Quiz', href: '#post2', icon: 'assignment_turned_in' },
        { name: 'Video', href: '#post3', icon: 'video_library' },
        { name: 'Article', href: '#post4', icon: 'library_books' }
      ]
    }
  },
  mounted () {
    new Typed('#greeting', {// eslint-disable-line no-new
      strings: this.typedOptions,
      loop: false,
      typeSpeed: 50,
      backSpeed: 10,
      startDelay: 3000,
      backDelay: 2000,
      smartBackspace: true,
      showCursor: false
    })
  }
//   computed: {
//     user () {
//       return this.$store.getters.user
//     },
//     error () {
//       return this.$store.getters.error
//     },
//     loading () {
//       return this.$store.getters.loading
//     },
//     comments () {
//       return this.$store.getters.comments
//     }
//   },
//   created () {
//     this.$store.dispatch('getComments')
//   },
//   methods: {
//     GoogleSignIn () {
//       this.$store.dispatch('userProvider', new firebase.auth.GoogleAuthProvider())
//     },
//     Logout () {
//       this.$store.dispatch('userLogout')
//     },
//     addComment (text, id) {
//       if (text !== '') {
//         this.$store.dispatch('addComment', {text: text, post: id, creator: this.user.id, name: this.user.name, photo: this.user.photo})
//         .then(this.$store.dispatch('getComments'))
//       }
//     },
//     deleteComment (text) {
//       this.$store.dispatch('deleteComment', text)
//       .then(this.$store.dispatch('getComments'))
//     }
//   }
// }
}
</script>

<style media="screen">
@import url('https://fonts.googleapis.com/css?family=Quicksand');
@import url('https://fonts.googleapis.com/css?family=Permanent+Marker');
@import url('https://fonts.googleapis.com/css?family=Indie+Flower');
*{
  font-family: 'Quicksand', sans-serif;
}
html{
  background: black;
}
a {
  text-decoration: none !important;
}
.v-input__slot {
  border-radius: 2em !important;
}
.video {
  -webkit-mask-image: -webkit-radial-gradient(circle, white 100%, black 100%); /*ios 7 border-radius-bug */
  -webkit-transform: rotate(0.000001deg); /*mac os 10.6 safari 5 border-radius-bug */
  -webkit-border-radius: 3em;
  -moz-border-radius: 3em;
  border-radius: 3em;
  overflow: hidden;
  z-index: 9;
  position: relative;
  padding-bottom: 57%; /* 16:9 */
  padding-top: 25px;
  height: 0;
}
.video iframe {
  position: absolute;
  top: 0;
  left: 0;
  width: 100%;
  height: 100%;
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
.round{
  border-radius: 2em;
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
@keyframes lightSpeedIn {
  from {
    transform: translate3d(100%, 0, 0) skewX(-30deg);
    opacity: 0;
  }

  60% {
    transform: skewX(20deg);
    opacity: 1;
  }

  80% {
    transform: skewX(-5deg);
    opacity: 1;
  }

  to {
    transform: none;
    opacity: 1;
  }
}
#title {
  font-family: 'Indie Flower', sans-serif;
  font-size: 3em;
  opacity: 0;
  animation: fadeInDown 1s 1s ease 1 forwards;
}
#face{
  opacity: 0;
  height: 30vh;
  width: 30vh;
  border-radius: 100%;
  animation: rollIn 1s 1.5s ease 1 forwards;
}
#info{
  opacity: 0;
  animation: lightSpeedIn 1s 1.5s ease 1 forwards;
}
.post{
  opacity:0;
  animation: fadeInUp 1s 2s ease 1 forwards;
}
.zoom{
  opacity:0;
  animation: zoomIn 1s 2s ease 1 forwards;
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
