<script>
export default {
    name: "FooterTop",
    props: {
        contact: Array,
        courses: Array
    }
}
</script>

<template>
    <section id="footer-top">
        <div class="container-lg py-5">
            <div class="row">
                <div class="col-3">
                    <img class="w-100" src="/logo-avada.png" alt="logo avada">
                    <p>
                        Avada Driving School is the right choice for
                        exwienced drivers looking for a refresher
                        course. Or the brand new driver wanting to
                        first time.
                    </p>
                </div>
                <div class="col-3">
                    <h3>CONTACT DETAILS</h3>
                    <ul class="p-0">
                        <li v-for="(element, index) in contact" class="d-flex" :key="index">
                            <i :class="element.icon"></i>
                            <span>{{ element.name }}</span>
                        </li>
                    </ul>
                </div>
                <div class="col-3">
                    <h3>COURSES</h3>
                    <ul class="p-0">
                        <li v-for="(course, index) in courses" :key="index">
                            <a href="#">
                                <i :class="course.icon"></i>
                                {{ course.name }}
                            </a>
                        </li>
                    </ul>
                </div>
                <div class="col-3 text-center">
                    <img class="w-100 pb-5" src="/rate.png" alt="rate rating">
                    <div>
                        <a class="ms_button" href="#">
                            BOOK NOW
                        </a>
                    </div>
                </div>
            </div>
        </div>
    </section>
</template>

<style lang="scss" scoped>
@use '../styles/partials/variables';
@use '../styles/partials/mixins';

#footer-top {
    background-image: url(/footer-bg.jpg);

    & .container-lg {

        & p {
            padding-top: 20px;
            color: variables.$color-grey;
            font-size: 14px;
        }

        & h3 {
            font-size: 18px;
            font-weight: 600;
            padding-bottom: 10px;
            color: variables.$color-white;
        }

        & .ms_button {
            @include mixins.button;
            text-decoration: none;
            font-weight: 600;

            &:hover {
                background-color: lighten(variables.$primary-color, 10);
            }

            &:active {
                background-color: darken(variables.$primary-color, 10);
            }
        }

        & ul li {
            list-style: none;
            font-size: 15px;
            padding: 0.5rem 0;
            color: variables.$color-grey;

            & a {
                text-decoration: none;
                color: variables.$primary-color;

                &:hover {
                    color: lighten(variables.$primary-color, 10);
                }
            }

            & i {
                padding-right: 1rem;
            }
        }
    }
}
</style>