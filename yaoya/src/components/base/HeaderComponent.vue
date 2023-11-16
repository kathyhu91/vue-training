<template>
  <header class="p-3 bg-success bg-opacity-25 mb-5">
    <nav class="navbar navbar-expand-lg">
      <div class="container-fluid d-flex justify-content-between align-items-center">
        <a
          class="navbar-brand text-decoration-none fs-3 link-success d-flex align-items-center"
          href="/"
        >
          <img :src="logoImg" alt="Logo" class="d-inline-block align-text-top brand---md" />
          <span class="ms-1">三木森八百屋</span>
        </a>
        <div class="nav-item">
          <RouterLink to="/shopping" class="nav-link"
            ><i class="bi bi-cart4 mx-1"></i>購物車</RouterLink
          >
        </div>
      </div>
    </nav>
  </header>
</template>

<script>
import { RouterLink } from 'vue-router'
import logoImg from '@/assets/img/logo.png'

export default {
  data() {
    return {
      logoImg: logoImg
    }
  },
  components: {
    RouterLink
  }
}
</script>
