<template>
  <span>
      <ebul-styles />
      <div class='backlayer' id="india"></div>
      <div class='backlayer' id="india-vector"></div>
      <main-container />
       <!-- <dics-viewer :showIndexes="true" :data="{name:'nikhilesh yadav',class:'cs2',sex:'male'}" along='vertical'/> -->
     <!-- <event-card :data="{type:'person-card',name:'mikey singh',timing:{from:'1 AM',to:'2 AM'},department:'CSE',fiveWords:'another event is here'}" viewMode="medium-card"/> -->
    <!-- <person-card :data="{type:'person-card',name:'mikey singh',eventsCount:3,department:'CSE'}" viewMode="small-card"/> 
  <photo-card :data="{src:'//192.168.43.249:8081/img/pramod.jpg',desc:'Another photo\'s complete description',fiveWords:'very short descriptioms',uploader:{name:'Some Person'},tags:['#pic','#picture']}" viewMode="medium-card"/> -->
  </span>
</template>

<script>
import mainContainer from './components/main-container.vue'
import personCard from './components/person-card-s-m'
import eventCard from './components/event-card-s-m'
import photoCard from './components/photo-card-s-m'
import dicsViewer from "./components/dics-viewer"
import ebulCard from "./components/card-s-m"
import thumbViewer from "./components/list-containers/thumb-viewer"
import ebulStyles from "./components/style-handle"
import listViewer from "./components/list-viewer"
export default {
  name: 'App',
  components: {
    mainContainer,
    personCard,
    eventCard,
    photoCard,
    dicsViewer,
    ebulCard,
    thumbViewer,
    ebulStyles,
    listViewer
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
.backlayer
{
    width: 100vw;
    height: 100vh;
    z-index: -1;
    position: fixed;
    background-repeat: no-repeat;
    opacity: 0.27;
}
#india
{
    background-image: url(./assets/india.png);
    background-position: left bottom;
    background-size: 197vh;
}
#india-vector
{
      background-image: url(./assets/india-vector.png);
      background-position: 30vw 62vh;
      background-size: 155vh
}
</style>
