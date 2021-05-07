<template>
<div class="discs-container flex">
    <div class="col"><div class="disc">test</div></div>
    <div class="col"><div class="disc">test</div></div>
    <div class="col"><div class="disc">test}</div></div>
    <div class="col"><div class="disc">{{ detail.name }}</div></div>
    <div class="col"><div class="disc">{{ detail.name }}</div></div>
    <div class="col"><div class="disc">{{ detail.name }}</div></div>
    <div class="col"><div class="disc">{{ detail.name }}</div></div>
    <div class="col"><div class="disc">{{ detail.name }}</div></div>
    <div class="col"><div class="disc">{{ detail.poster }}</div></div>
    <div class="col"><div class="disc">{{ detail.name }}</div></div>

</div>
</template>

<script>


export default {
    name: "DiscCollection",
    props: ["detail"],

}
</script>

<style lang="scss">

   .discs-container {
        justify-content: space-around;
        .col {
        flex-basis: calc(100% / 8 - 10px);
        margin-top: 5rem;
        background-color: rgb(87, 187, 154);
        border: 1px solid purple;
        }
    } 

    .disc {
        height: 80px;
    }
    
</style>