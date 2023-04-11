<template>
  <header>
    <HeaderTop />
    <HeaderJumbotron :nav="navLinks" />
  </header>

  <main>
    <SectionCallback />
  </main>
  <footer>

  </footer>
</template>

<script>
import HeaderTop from './components/HeaderTop.vue';
import HeaderJumbotron from './components/HeaderJumbotron.vue';
import SectionCallback from './components/SectionCallback.vue';
import PageFooter from './components/PageFooter.vue';

export default {
  components: {
    HeaderTop,
    HeaderJumbotron,
    SectionCallback,
    PageFooter
  },
  data() {
    return {
      navLinks: [
        {
          href: "#home",
          text: "home"
        },
        {
          href: "#about",
          text: "about"
        },
        {
          href: "#prices",
          text: "prices"
        },
        {
          href: "#courses",
          text: "courses"
        },
        {
          href: "#locations",
          text: "locations"
        },
        {
          href: "#blog",
          text: "blog"
        }
      ]
    }
  }
}
</script>


<style lang="scss">
@use "./styles/general.scss" as *;
</style>
