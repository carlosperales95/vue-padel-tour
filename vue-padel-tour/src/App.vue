<template>
  <div class="base-container">
    <!-- <app-header /> -->
    <router-view/>
  </div>
</template>

<script>
// import AppHeader from '@/components/AppHeader.vue'

export default {
  components: {
    // AppHeader
  }
}
</script>

<style scoped lang="scss">
h3 {
  margin: 40px 0 0;
}
ul {
  list-style-type: none;
  padding: 0;
}
li {
  display: inline-block;
  margin: 0 10px;
}
a {
  color: #fff;
}

.base-container {
  color: #fff;
  background-color: #14251C;
}

</style>
