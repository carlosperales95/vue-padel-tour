<template>
  <div class="home">
    <SplashContent />
    <RegisterButton/>
  </div>
</template>

<script lang="ts">
import { defineComponent } from 'vue'
import SplashContent from '@/components/SplashContent.vue' // @ is an alias to /src
import RegisterButton from '@/components/RegisterButton.vue' // @ is an alias to /src

export default defineComponent({
  name: 'HomeView',
  components: {
    SplashContent,
    RegisterButton
  }
})
</script>

<style lang="scss">
  .home {
    background-color: #9db7a9;
    width: 100%;
    height: 100%;
  }
</style>
