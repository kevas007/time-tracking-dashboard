<template>
    <div class="app">
        <div class="title">
            <div class="div" v-bind:style="{background:color}">
                <img  :src="img"
                alt />
            </div>
            <div class="sous">
                <h4>{{data.title }}</h4>
            <div v-if="ar == 'daily'">
            <h1>{{data.timeframes.daily.current }}hrs</h1>
            <h4>Last Day : {{ data.timeframes.daily.previous }}hrs</h4>
            </div>
            <div  v-else-if="ar == 'weekly'">
                <h1>{{data.timeframes.weekly.current }}hrs</h1>
            <h4>Last Week: {{ data.timeframes.weekly.previous }}hrs</h4>
            </div>
            <div  v-else-if="ar == 'monthly'">
                <h1>{{data.timeframes.monthly.current }}hrs</h1>
            <h4>Last Month :{{ data.timeframes.monthly.previous }}hrs</h4>
            </div>
            </div>

        </div>
    </div>
</template>

<script>

export default {

    data() {
        return {

            // title: 'Travail',
            // current: 5,
            // previous: 7,
            // img: require('../assets/images/icon-work.svg')

        }
    },
props: {
    data: {
        type: Object,
        required: true
    },
    img: {
        type: String,
        required: true
    },
    color: {
        type: String,
        required: true
    },
    ar:{
        type: String,
        required: true
    }
},

}
</script>
<style scoped>
.app{
    display:flex;
    flex-direction:row;
    flex-wrap: wrap;
    justify-content:space-between;
   
}
.title {
    color: white;
    display: flex;
    flex-direction: column;
    justify-content: center;
    align-items: center;
    background: rgb(24, 1, 66);
    border-radius: 10px;
    width: 100%;
    height: 100%;
    margin-left: 5%;
    margin-right: 5%;
    

}
.div{
    /* background: rgb(24, 1, 66); */
    border-radius: 10px;
;
}
</style>