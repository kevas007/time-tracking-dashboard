<template>
  <div id="app">
  <SideBar class="sideBar" @change="update" />
  <Study class="study" :ar="arrays" v-for="(data, index ) in datas" :key="data.title" :data="data" :img="image[index]" :color="colors[index]"/>

  </div>
</template>

<script>
import data from '../exo-ressources/data.json';
import SideBar from './Components/SideBar.vue'
import Study from './Components/Study.vue';
export default {
    name: "App",

    data() {
        return {
        datas: data,
        image: [
                require('./assets/images/icon-work.svg'),
                require('./assets/images/icon-play.svg'),
                require('./assets/images/icon-study.svg'),
                require('./assets/images/icon-exercise.svg'),
                require('./assets/images/icon-social.svg'),
                require('./assets/images/icon-self-care.svg'),
            ],
            colors: [
                'hsl(15, 100%, 70%)',
                'hsl(195, 74%, 62%)',
                'hsl(348, 100%, 68%)',
                'hsl(145, 58%, 55%)',
                'hsl(264, 64%, 52%)',
                'hsl(43, 84%, 65%)',
            ],
          title: 'Report for',
            subtitle: 'Jeremy Robson',
            arrays:"daily",
        };
    },
    methods: {
        update(value) {
            this.arrays = value;
          console.log(this.arrays);
        }
    },
    components: { Study, SideBar }
}
</script>



<style lang="sass">
body
  background-color:  hsl(235, 46%, 20%)
#app
    display: grid
    grid-template-columns: repeat(4,240px)
    grid-template-rows: repeat(2,240px)
    grid-gap: 25px
.sideBar
    grid-column: 1/2
    grid-row: 1/3
.apps
    position: relative
.study
  width: 240px
  height: 240px
  margin-left:15% 
.sub
    font-size: 1.5em
    font-weight: bold
    margin-bottom: 100px

.card-image
    width: 28%
    height: 30%
    border: 3px solid white
    border-radius: 50%
    margin-top: 5%
    margin-bottom: 5%

.cards 
    background-color: rgb(20, 18, 138)
    display: flex
    flex-direction: column
    justify-content: start
    /* align-items: center; */
    margin-top: 35px
    padding-left: 35px
    width: 300px
    color: white
    border-radius: 5%
    /* width: 15%; */
    z-index: 10

.card 

    background-color: rgb(25, 12, 99)
    display: flex
    flex-direction: column
    justify-content: start
    /* align-items: center; */
    /* margin-top: 20px; */
    padding-left: 35px
    width: 300px
    color: white
    border-radius: 5%
    /* width: 15%; */
  

</style>
