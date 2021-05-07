<template>
  <div id="app">
    <header>
        <Header />
    </header>
    <main>
        <Main />
    </main>
  </div>
</template>

<script>
import Header from '@/components/Header.vue';
import Main from '@/components/Main.vue';


export default {
  name: 'App',
  components: {
    Header,
    Main,
  }
}
</script>

<style lang="scss">
@import "./assets/styles/vars.scss";

#app {
    background-color: $darkerblue;
}
</style>
