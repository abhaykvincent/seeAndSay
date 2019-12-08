<template>
    <div id="canvas">
        <h3 id="canvasHeading">Select one Vowel and Learn</h3>
        <div id="tiles">
            <div class="tiles" v-for="(item, index) in tiles" :key="index"  @click="addHistory(item)">{{item}}</div>
        </div>
    </div>
</template>

<script>

export default {
    name: "Tiles",
    props: {
        tiles: {
            type: Array,
        },
        history: {
            type: Array,
        }
    },
    methods: {
        addHistory(letter) {
            if(this.history.length<10)
                this.history.push(letter)
            else
            {
                this.history.splice(0,1);
                this.history.push(letter)
            }
        },
    },
}
</script>
<style >
    #tiles
    {
        position: relative;
        width: 40vw;
        margin: 0px 30vw;
        display: table;
    }
    .tiles{
        float: left;
        width: 8vw;
        height: 8vw;
        margin: 1vw 0px;
        border-radius: 50%;
        background-color : rgb(233, 191, 157); 
    }

    .tiles:nth-child(even){
        margin-top: 8vw;
    }
    .tiles:nth-child(odd){
        margin-bottom: 8vw;
    }
</style>