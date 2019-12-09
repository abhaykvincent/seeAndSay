<template>
    <div id="canvas">
        <h3 id="canvasHeading">Select one Vowel and Learn</h3>
        <div id="tiles">
            <div class="tiles" v-for="(item, index) in tiles" :key="index" @click="$emit('playAudio', index);addHistory(item.letter,index)">
                <img :src="item.img"/>
            </div>
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
        addHistory(letter,index) {
            let item={"letter":letter,"hisIndex":index};
            if(this.history.length<10)
                this.history.push(item)
            else
            {
                this.history.splice(0,1);
                this.history.push(item)
            }
        },/* 
        addImg(letter) {
            if(this.history.length<10)
                this.history.push(letter)
            else
            {
                this.history.splice(0,1);
                this.history.push(letter)
            }
        } */
    },
  
    mounted(){
    var letterImg = document.getElementsByClassName("hide");
    for(var i = 0; i < letterImg.length; i++)
    {
        this.tiles[i].img=letterImg[i].src;
    }
    }
}
</script>
<style >
#canvasHeading{
    display: inline-block;
    padding: 10px 20px;
    border-radius: 5px;
    background-color: #f5dfce;

}
    #tiles
    {
        position: relative;
        padding: 40px;
        width: 40vw;
        margin: 0px calc(30vw - 40px);
        display: table;
        border-radius: 20px;
        background-color: #f5dfce;
    }
    .tiles{
        float: left;
        width: 8vw;
        height: 8vw;
        margin: 1vw 0px;
        border-radius: 50%;
        background-color : #eccbb1
    }
    .tiles:hover
    {
        background-color: #cea789;
        cursor: pointer;
    }
    .tiles:hover > img{
        width: 100%;
        margin: 0px;
        cursor: pointer;
    }
    .tiles img{
        width: 90%;
        margin: 5%;
        transition-duration: 0.2s
    }

    .tiles:nth-child(even){
        margin-top: 8vw;
    }
    .tiles:nth-child(odd){
        margin-bottom: 8vw;
    }
</style>