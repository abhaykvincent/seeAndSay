<template>
    <div id="credits">
        <p v-for="(item, index) in credits" :key="index">{{item.name}} : 
            <span v-for="(element, indexB) in item.list" :key="indexB">{{element}},
            </span>
        </p>
    </div>
</template>
<script>

export default {
    name: "Credits",
    props: {
        credits: {
            type: Object,
        },
    },
}
</script>
<style>

    #credits
    {
    width: 100vw;
    background-color: rgb(243, 88, 88)
    }
</style>