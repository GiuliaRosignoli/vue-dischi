<template>
<div class="single-disc">
    <img v-bind:src="detail.poster" alt="detail.title">
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
@import "../assets/styles/vars.scss";

   .single-disc {
        width: calc(100% / 8 - 10px);
        margin: 20px 0;
        background-color: $lighterblue;
        img {
            width: 120px;
        }
    } 

    
</style>