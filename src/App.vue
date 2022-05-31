<template>
  <div class="wrapper">
    <div class="container">
      <Header />
      <main class="wrapper-content">
        <router-view />
      </main>
      <Footer />
    </div>
  </div>
</template>

<script lang="ts">
import Header from '@/components/Header.vue'
import Footer from '@/components/Footer.vue'

export default {
  components: { Header, Footer }
}
</script>

<style></style>
