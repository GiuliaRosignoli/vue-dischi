<template>
    <section class="discs">
        <DiscCollection v-for="(disc, index) in collections" v-bind:key="index" :detail="disc" />
    </section>
  
</template>

<script>
import DiscCollection from "@/components/DiscCollection.vue"
export default {
    name: "Main",
    components: {
        DiscCollection,
    },
    data(){
        return {
            collections: [
                {
                    name: "Innuendo",
                    singer: "Queen",
                }
            ],
        }
    }
}
</script>

<style lang="scss" scoped>
@import "../assets/styles/general.scss"; 
@import "../assets/styles/vars.scss";
@import "../assets/styles/utilities.scss";

.discs {
    height: 600px;
    background-color: $darkerblue;
}



</style>