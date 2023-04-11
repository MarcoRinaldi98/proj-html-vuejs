<template>
  <header>
    <HeaderTop />
    <HeaderJumbotron :nav="navLinks" />
  </header>

  <main>
    <SectionCallback />
    <SectionContactUs />
    <SectionCourses />
    <SectionRate />
    <SectionAbout />
    <SectionTestimonials />
    <SectionBlog />
  </main>
  <footer>

  </footer>
</template>

<script>
import HeaderTop from './components/HeaderTop.vue';
import HeaderJumbotron from './components/HeaderJumbotron.vue';
import SectionCallback from './components/SectionCallback.vue';
import SectionContactUs from './components/SectionContactUs.vue';
import SectionCourses from './components/SectionCourses.vue';
import SectionRate from './components/SectionRate.vue';
import SectionAbout from './components/SectionAbout.vue';
import SectionTestimonials from './components/SectionTestimonials.vue';
import SectionBlog from './components/SectionBlog.vue';
import PageFooter from './components/PageFooter.vue';

export default {
  components: {
    HeaderTop,
    HeaderJumbotron,
    SectionCallback,
    SectionContactUs,
    SectionCourses,
    SectionRate,
    SectionAbout,
    SectionTestimonials,
    SectionBlog,
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
