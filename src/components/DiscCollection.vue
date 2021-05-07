<template>
<div class="single-disc">
    <h2>{{detail.title}}</h2>
    <h3>{{detail.author}}</h3>
    <h4>{{detail.year}}</h4>
    <h4>{{detail.genre}}</h4>
</div>
</template>

<script>


export default {
    name: "DiscCollection",
    props: ["detail"],

}
</script>

<style lang="scss">

   .single-disc {
        flex-basis: 100px;
        margin: 20px 0;
        background-color: #fff;

    } 

    
</style>