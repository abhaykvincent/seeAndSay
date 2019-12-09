<template>
    <div id="history">
        <h3>Last Choices By you</h3>
        <div id="historyTiles">
            <div class="historyTiles" v-for="(item, index) in history"  :key="index">
                <img :src="tiles[item.hisIndex].img"/>
            </div>
        </div>
            
    </div>
</template>
<script>

export default {
    name: "History",
    props: {
        tiles: {
            type: Array,
        },
        history: {
            type: Array,
        }
    },
}
</script>
<style>

    #history
    {
        position: relative;
        display: table;
        width: 100vw;
        background-color: rgba(243, 88, 88,0);

    }
    #history h3{
        margin: 10px;
        margin-top: 30px;
    display: inline-block;
    padding: 10px 20px;
    border-radius: 5px;
    background-color: #f5dfce;

    }
    #historyTiles
    {
        display: table;
        margin-left: 50%;
        transform: translateX(-50%);
        background-color:rgb(243, 88, 88);
        border-radius: 5px;
        margin-bottom: 20px;
    }
    .historyTiles{
        float: left;
        width: 50px;
        height: 50px;
        margin: 5px;
    padding: 5px;
        border-radius: 50%;
        background-color : rgb(233, 191, 157);
        background-color : rgb(233, 191, 157); 
    }
</style>