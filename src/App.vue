<template>
  <div id="app" v-cloak>
    <Header />
    <div class="app-content">
      <router-view/>
    </div>
    <Footer loading="lazy" />
    <GoTop />
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
#app {
  max-width: 100%;
  overflow-x: hidden;
}
.app-content {
  min-height: 2000px;
}
</style>
