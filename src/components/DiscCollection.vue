<template>
    <div class="single-disc">
        <img v-bind:src="detail.poster" alt="detail.title">
        <h2>{{detail.title}}</h2>
        <h3>{{detail.author}}</h3>
        <h4>{{detail.year}}</h4>
        <h5>{{detail.genre}}</h5>
    </div>
</template>

<script>

export default {
    name: "DiscCollection",
    props: ["detail"],

}
</script>

<style lang="scss">
@import "../assets/styles/general.scss"; 
@import "../assets/styles/vars.scss";
@import "../assets/styles/utilities.scss";


   .single-disc {
        width: calc(100% / 8 - 10px);
        margin: 20px 0;
        background-color: $lighterblue;
        img {
            width: 120px;
            padding: 12px;
        }
    } 


    
</style>