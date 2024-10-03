<template>
  <header>
    <Navbar />
    <HambugerMenu />
  </header>
  <router-view />
  <footer>
    <Footer />
  </footer>
</template>

<script>
import Navbar from '@/components/layout/NavbarModel.vue';
import HambugerMenu from '@/components/layout/HambugerMenu.vue';
import Footer from '@/components/layout/FooterModel.vue';

export default {
  components: { Navbar, HambugerMenu, Footer },
};
</script>
