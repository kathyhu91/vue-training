<template>
  <div class="wrap">
    <HeaderComponent></HeaderComponent>
    <RouterView />
    <FooterComponent></FooterComponent>
  </div>
</template>
<script>
import { RouterView } from 'vue-router'
import HeaderComponent from './components/base/HeaderComponent.vue'
import FooterComponent from './components/base/FooterComponent.vue'

export default {
  components: {
    RouterView,
    HeaderComponent,
    FooterComponent
  }
}
</script>
