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
            apiURL: "https://flynn.boolean.careers/exercises/api/array/music",
            discList: [],
            loading: true,
        }
    },
    created(){
        this.getDisc();
    },
    methods: {
        getDisc() {
            axios.get(this.apiURL)
            .then(res=>{
                console.log(res.data)
            })
            .catch(err=>{
                console.log('Error:', err)
            })
        }
    }
}
</script>
import axios from "axios";

<style lang="scss" scoped>
@import "../assets/styles/general.scss"; 
@import "../assets/styles/vars.scss";
@import "../assets/styles/utilities.scss";

.discs {
    height: 600px;
    background-color: $darkerblue;
}



</style>