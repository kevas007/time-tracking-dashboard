<template>
    <div class="apps">
        <div class="cards">
            <img src="../assets/images/image-jeremy.png" alt />

            <div>
                <p>{{ title }}</p>
                <h1>{{ subtitle }}</h1>
            </div>
        </div>

        <div class="card">
            <h4><button :class="{'blanc': check=='daily'}" @click="change('daily')" >Daily</button></h4>
            <h5><button :class="{'blanc': check=='weekly'}" @click="change('weekly')">Weekly</button></h5>
            <h5><button :class="{'blanc': check=='monthly'}"  @click="change('monthly')">Monthly</button></h5>
        </div>
    </div>
</template>

<script>
export default {
    name: 'SideBar',
    props: {
        Daily: {
            type: String,
            default: 'Daily'
        },
        Weekly: {
            type: String,
            default: 'Weekly'
        },
       Monthly: {
            type: String,
            default: 'Monthly'
        },
    },
    data() {
        return {
            check:'',
            title: 'Report for',
            subtitle: 'Jeremy Robson'
        }
    },
    methods: {
        change(value) {
            this.$emit('change', value)
            this.check = value
        }
    }

}
</script>
<style scoped>
.blanc {
    background-color: blue;
}
.apps{
    position: relative;
}
h1{
    font-size: 1.5em;
    font-weight: bold;
    margin-bottom: 100px;
}
img {
    width: 28%;
    height: 30%;
    border: 3px solid white;
    border-radius: 50%;
    margin-top: 5%;
    margin-bottom: 5%;
}
.cards {
    background-color: rgb(20, 18, 138);
    display: flex;
    flex-direction: column;
    justify-content: start;
    /* align-items: center; */
    margin-top:0;
    width: 100%;
    color: white;
    border-radius: 5%;
    /* width: 15%; */
  
    
}
.card {


    background-color: rgb(25, 12, 99);
    display: flex;
    flex-direction: column;
    justify-content: start;
    /* align-items: center; */
    /* margin-top: 20px; */
    width: 100%;
    color: white;
    border-radius: 5%;
    /* width: 15%; */
    z-index: 1;
    }
</style>