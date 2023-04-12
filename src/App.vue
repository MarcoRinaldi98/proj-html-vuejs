<template>
  <header>
    <HeaderTop />
    <HeaderJumbotron :nav="navLinks" />
  </header>

  <main>
    <SectionCallback />
    <SectionContactUs />
    <SectionCourses :type="coursesType" />
    <SectionRate />
    <SectionAbout :instructors="instructorList" />
    <SectionTestimonials :testimonials="testimonalsList" />
    <SectionBlog />
    <SectionNewsletter />
  </main>
  <footer>
    <FooterTop :contact="contactList" :courses="courseList" />
    <FooterBottom :social="socialList" />
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
import SectionNewsletter from './components/SectionNewsletter.vue';
import FooterTop from './components/FooterTop.vue';
import FooterBottom from './components/FooterBottom.vue';

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
    SectionNewsletter,
    FooterTop,
    FooterBottom
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
      ],
      socialList: [
        {
          type: 'fa-brand',
          name: 'fa-facebook-f'
        },
        {
          type: 'fa-brand',
          name: 'fa-twitter'
        },
        {
          type: 'fa-brand',
          name: 'fa-youtube'
        },
        {
          type: 'fa-brand',
          name: 'fa-instagram'
        }
      ],
      contactList: [
        {
          icon: 'fa-solid fa-house-chimney-window',
          name: '12345, North Main Street, New York, NY 5555555'
        },
        {
          icon: 'fa-solid fa-phone-flip',
          name: '1.800.555.6789'
        },
        {
          icon: 'fa-regular fa-envelope',
          name: 'info@your-domain.com'
        },
        {
          icon: 'fa-solid fa-link',
          name: 'Theme-Fusion.com'
        }
      ],
      courseList: [
        {
          icon: 'fa-regular fa-circle-right',
          name: 'Pass Plus'
        },
        {
          icon: 'fa-regular fa-circle-right',
          name: 'Intensive Course'
        },
        {
          icon: 'fa-regular fa-circle-right',
          name: 'Automatic'
        },
        {
          icon: 'fa-regular fa-circle-right',
          name: 'Instructor Training'
        }
      ],
      instructorList: [
        {
          img: '/about1.jpg',
          name: 'Mike Hart',
          social: [
            {
              icon: 'fa-brands fa-facebook-f',
              href: '#'
            },
            {
              icon: 'fa-brands fa-twitter',
              href: '#'
            },
            {
              icon: 'fa-brands fa-instagram',
              href: '#'
            }
          ],
          description: 'Lorem ipsum dolor sit amet, consectetur adipiscing elit.'
        },
        {
          img: '/about2.jpg',
          name: 'John Smith',
          social: [
            {
              icon: 'fa-brands fa-facebook-f',
              href: '#'
            },
            {
              icon: 'fa-brands fa-twitter',
              href: '#'
            },
            {
              icon: 'fa-brands fa-instagram',
              href: '#'
            }
          ],
          description: 'Lorem ipsum dolor sit amet, consectetur adipiscing elit.'
        },
        {
          img: '/about3.jpg',
          name: 'Angela Hart',
          social: [
            {
              icon: 'fa-brands fa-facebook-f',
              href: '#'
            },
            {
              icon: 'fa-brands fa-twitter',
              href: '#'
            },
            {
              icon: 'fa-brands fa-instagram',
              href: '#'
            }
          ],
          description: 'Lorem ipsum dolor sit amet, consectetur adipiscing elit.'
        }
      ],
      coursesType: [
        {
          name: 'Pass Plus',
          image: '/courses1.jpg'
        },
        {
          name: 'Intensive Course',
          image: '/courses2.jpg'
        },
        {
          name: 'Instructors',
          image: '/courses3.jpg'
        }
      ],
      testimonalsList: [
        {
          img: '/testimonial-sophia.png',
          name: 'Sophia Jones',
          dichiarazione: "Avado D'iving School really helped build my confidence behind the wheel and with driving in generon ond they got me a first time poss! Highly recammended."
        },
        {
          img: '/testimonial-kelly.png',
          name: 'Kelly Robertson',
          dichiarazione: "Avado D'iving School really helped build my confidence behind the wheel and with driving in generon ond they got me a first time poss! Highly recammended."
        },
        {
          img: '/testimonial-kate.png',
          name: 'Kate Will',
          dichiarazione: "Avado D'iving School really helped build my confidence behind the wheel and with driving in generon ond they got me a first time poss! Highly recammended."
        },
        {
          img: '/testimonial-harold.png',
          name: 'Harold Beni',
          dichiarazione: "Avado D'iving School really helped build my confidence behind the wheel and with driving in generon ond they got me a first time poss! Highly recammended."
        },
        {
          img: '/testimonial-grant.png',
          name: 'Grant Hart',
          dichiarazione: "Avado D'iving School really helped build my confidence behind the wheel and with driving in generon ond they got me a first time poss! Highly recammended."
        }
      ]
    }
  }
}
</script>


<style lang="scss">
@use "./styles/general.scss" as *;
</style>
