<template>
    <div id="heading"><h1>{{heading}}</h1></div>
</template>
<script>

export default {
    name: "Heading",
    props: {
        heading: {
            type: String,
        },
    },
    mounted(){
    var HeaderImg = document.getElementById("header");
        HeaderImg.style.background= 'url(https://i.ytimg.com/vi/C2Vwn3pxUPg/maxresdefault.jpg)';
    }
}
</script>
<style>

    #heading
    {
    height: 100px;
    width: 100vw;
    margin:0px;
    line-height: 100px;
    background-color: rgb(243, 88, 88)
    }
    #heading h1
    {
    margin:0px;
    color: #ffe55e;
    }
</style>