<template>
    <section class="wrapper">
        <div>
            <Search @performSearch="searchDisc" />
        </div>
        <div class="disc-section flex"> <!--loop -->
            <DiscCollection v-for="(disc, index) in collections" v-bind:key="index" :detail="disc" />
        </div>
    </section>
  
</template>

<script>
import axios from "axios";
import DiscCollection from "@/components/DiscCollection.vue";
import Search from "@/components/Search.vue";

export default {
    name: "Main",
    components: {
        DiscCollection,
        Search,
    },
    data(){
        return {
            apiURL: "https://flynn.boolean.careers/exercises/api/array/music",
            collections: [],
            searchingDiscs: "",
        }
            
    },
    computed: {
        filteredDiscList(){
            if(this.searchingDiscs === ""){
                return this.collections
            }
            return this.collections.filter(item =>{
                return item.name.toLowerCase.includes(this.searchingDiscs.toLowerCase());
            })
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
        },
        searchDisc(text) {
            console.log("Text inserted: ", text);

            this.searchingDiscs = text;

        }
    }
}
</script>


<style lang="scss" scoped>
@import "../assets/styles/general.scss"; 
@import "../assets/styles/vars.scss";
@import "../assets/styles/utilities.scss";


.wrapper {
    height: calc(100vh - 3.5rem );
    align-items: flex-start;
    flex-wrap: wrap;
    .disc-section {
        justify-content: center;
        flex-wrap:wrap;
        width: 100%;
        margin-top: 60px;
        padding: 15px;
    }
}




</style>