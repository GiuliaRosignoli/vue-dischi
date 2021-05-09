<template>
    <div class="single-disc flex">
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
        flex-direction: column;
        align-items: center;
        margin-bottom: 10px;
        justify-items: center;
        flex-basis: calc(100% / 8 - 20px);
        padding-bottom: 10px;
        background-color: $lighterblue;
        img {
            width: 120px;
            padding: 12px;
        }
    } 


    
</style>