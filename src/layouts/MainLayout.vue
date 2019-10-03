<template>
  <div class="main-layout">
  <CoreNavbar />
    <router-view />
  </div>
</template>

<script>
  export default {
    name: 'main-layout',
    components: {
      CoreNavbar: () => import('@/core/Navbar'),
      // CoreFooter: () => import('@/core/Footer')
    }
  }
</script>
