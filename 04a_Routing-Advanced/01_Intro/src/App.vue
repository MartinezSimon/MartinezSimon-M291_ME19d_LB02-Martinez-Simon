<template>
  <!--
    Basic router navigation
    Update navigation by adding two router links for Home and About
   -->
  <div id="app">
    <div id="logo"><img class="logo" alt="logo" src="./assets/logo.png"></div>
    <div id="nav">
      <router-link to="/home">Home | Start</router-link> |
      <router-link to="/message">Message</router-link> |
      <router-link to="/messages">Feed</router-link> |
      <router-link :to="{ name: 'about', params: { user: 'The Geneva International Motor Show (GIMS) is a not-for-profit foundation based in Geneva, Switzerland. It is independent, impartial and has no political affiliation.\n'+
'\n'+
'The Geneva International Motor Show is one of the most prestigious and influential events in the automotive world. It is also the only show in Europe recognised by the International Organization of Motor Vehicle Manufacturers (OICA). The GIMS attracts over 10,000 journalists and more than 600,000 visitors to Geneva for every event.\n'+
'\n'+
'The Geneva Motor Show’s privileged position is due not only to its renowned organisational arrangements and Geneva’s international reputation, but also the unique role played by Switzerland, which is practically the only country in the world where there is free competition without quotas in the private motor vehicle trade. The Geneva Motor Show is therefore an even more international event than the other four manufacturers’ shows (in Paris, Munich, Tokyo and Detroit), which all promote domestic production.'}}">About GIMS</router-link>
    </div>
    <router-view/>
    <MyNavigation />
  </div>
</template>

<script>
/* Import all components */
import SimpleNav from './components/SimpleNav'

export default {
  components: {
    MyNavigation: SimpleNav,
  },
}
</script>

<style lang="scss">
//Import of global-style
@import 'styles/global';
</style>

