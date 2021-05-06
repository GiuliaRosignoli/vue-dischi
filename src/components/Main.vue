<template>
    <section class="discs">
        <DiscCollection v-for="(items, index) in DiscCollection v-bind:key="index" detail="disc" />
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

        }
    }
}
</script>

<style lang="scss" scoped>
@import "../assets/styles/general.scss"; 
@import "../assets/styles/vars.scss";
@import "../assets/styles/utilities.scss";

</style>