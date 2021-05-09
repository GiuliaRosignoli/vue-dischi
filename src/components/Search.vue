<template>
  <div class="search">
      <input type="text" placeholder="Search">
      <button class="mg">Search</button>
      <button>Reset</button>
  </div>
</template>

<script>
export default {
    name: "Search",
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

.search {
    padding-top: 30px;
    text-align: center;
    input {
        height: 1.8rem;
    }
}

button {
    margin: 5px;
    padding: 5px 9px;
    border-radius: 30%;
}

</style>