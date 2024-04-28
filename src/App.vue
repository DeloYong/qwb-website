<template>
  <div id="app" v-cloak>
    <Header></Header>
    <router-view/>
    <Footer></Footer>
    <GoTop></GoTop>
  </div>
</template>

<script>
export default {
  name: 'App'
}
</script>

<style>
[v-cloak] {
  display: none;
}
</style>
