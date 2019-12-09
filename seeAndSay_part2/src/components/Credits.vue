<template>
    <div id="credits">
        <p v-for="(item, index) in credits" :key="index">{{item.name}} : 
            <span v-for="(element, indexB) in item.list"  :key="indexB">{{element}}<span v-if="indexB!=item.list.length-1">, </span>
            </span>
        </p>
    </div>
</template>
<script>

export default {
    name: "Credits",
    props: {
        credits: {
            type: Array,
        },
    },
}
</script>
<style>

    #credits
    {
    padding: 30px;
    width: 100vw;
    font-weight: 600;
    color : white;
    background-color: rgb(243, 88, 88)
    }
    #credits p {
        margin: 5px 0px;
    }
</style>