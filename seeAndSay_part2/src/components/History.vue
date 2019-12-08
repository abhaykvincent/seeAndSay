<template>
    <div id="history">
        <h3>Last Choices By you</h3>
        <div id="historyTiles">
            <div class="historyTiles" v-for="(item, index) in history"  :key="index">{{item}}</div>
        </div>
            
    </div>
</template>
<script>

export default {
    name: "History",
    props: {
        history: {
            type: Array,
        },
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
    #historyTiles
    {
        display: table;
        margin-left: 50%;
        transform: translateX(-50%);
        background-color: rgba(243, 88, 88,1);
        border-radius: 5px;
    }
    .historyTiles{
        float: left;
        width: 50px;
        height: 50px;
        margin: 5px;
        border-radius: 50%;
        background-color : rgb(233, 191, 157);
        background-color : rgb(233, 191, 157); 
    }
</style>