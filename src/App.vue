<template>
  <header>
    <PageHeaderTop />
    <PageHeaderBottom :nav="navLinks" />
  </header>

  <main>

  </main>
  <footer>

  </footer>
</template>

<script>
import PageHeaderTop from './components/PageHeaderTop.vue';
import PageHeaderBottom from './components/PageHeaderBottom.vue';
import PageMain from './components/PageMain.vue';
import PageFooter from './components/PageFooter.vue';

export default {
  components: {
    PageHeaderTop,
    PageHeaderBottom,
    PageMain,
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
