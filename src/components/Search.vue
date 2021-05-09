<template>
  <div class="search">
      <input type="text">
  </div>
</template>

<script>
export default {
    name: "Search",
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

</style>