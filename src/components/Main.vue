<template>
    <section class="wrapper">
        <div class="disc-section flex"> 
            <DiscCollection v-for="(disc, index) in collections" v-bind:key="index" :detail="disc" />
        </div>
    </section>
  
</template>

<script>
import axios from "axios";
import DiscCollection from "@/components/DiscCollection.vue"

export default {
    name: "Main",
    components: {
        DiscCollection,
    },
    data(){
        return {
            apiURL: "https://flynn.boolean.careers/exercises/api/array/music",
            collections: [],
        }
            
    },
    created(){
        this.getDisc()
    },
    methods: {
        getDisc() {
            axios.get(this.apiURL)
            .then(res=>{
                console.log(res.data);
                this.collections= res.data.response;

            })
            .catch(err=>{
                console.log('Error:', err)
            })
        }
    }
}
</script>


<style lang="scss" scoped>
@import "../assets/styles/general.scss"; 
@import "../assets/styles/vars.scss";
@import "../assets/styles/utilities.scss";

.wrapper {
    height: 100vh;
    align-items: flex-start;

    .disc-section {
        width: 100%;
        justify-content: space-around;
        margin-top: 60px;
    }
}




</style>