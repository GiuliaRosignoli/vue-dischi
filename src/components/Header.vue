<template>
    <div id="app"> 
       <header class="header">
           <div class="logo"><img src="../assets/img/logo.png" alt=""></div>
       </header>
    </div>
</template>

<script>

export default {
    name: "Header",
}
</script>

<style lang="scss" scoped>
@import "../assets/styles/general.scss"; 
@import "../assets/styles/vars.scss";
@import "../assets/styles/utilities.scss";



.header {
    height: 3.5rem;
    background-color: $lighterblue;
}

.logo img {
    width: 3rem;
    padding: 0.2rem;
}

</style>