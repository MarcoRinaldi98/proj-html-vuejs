<script>
export default {
    name: "FooterTop"
}
</script>

<template>
    <section id="footer-top">
        <div class="container-sm py-5">
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
                        <li class="d-flex">
                            <i class="fa-solid fa-house-chimney-window"></i>
                            <span>12345, North Main Street, New York, NY 5555555</span>
                        </li>
                        <li class="d-flex">
                            <i class="fa-solid fa-phone-flip"></i>
                            <span>1.800.555.6789</span>
                        </li>
                        <li class="d-flex">
                            <i class="fa-regular fa-envelope"></i>
                            <span>info@your-domain.com</span>
                        </li>
                        <li class="d-flex">
                            <i class="fa-solid fa-link"></i>
                            <span>Theme-Fusion.com</span>
                        </li>
                    </ul>
                </div>
                <div class="col-3">
                    <h3>COURSES</h3>
                    <ul class="p-0">
                        <li>
                            <a href="#">
                                <i class="fa-regular fa-circle-right"></i>
                                Pass Plus
                            </a>
                        </li>
                        <li>
                            <a href="#">
                                <i class="fa-regular fa-circle-right"></i>
                                Intensive Course
                            </a>
                        </li>
                        <li>
                            <a href="#">
                                <i class="fa-regular fa-circle-right"></i>
                                Automatic
                            </a>
                        </li>
                        <li>
                            <a href="#">
                                <i class="fa-regular fa-circle-right"></i>
                                Instructor Training
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

    & .container-sm {

        & p {
            padding-top: 20px;
            color: variables.$extra-color7;
        }

        & h3 {
            font-size: 22px;
            padding-bottom: 20px;
            color: variables.$color-white;
        }

        & .ms_button {
            @include mixins.button;
            text-decoration: none;
        }

        & ul li {
            list-style: none;
            font-size: 17px;
            padding: 0.5rem 0;
            color: variables.$extra-color7;

            & a {
                text-decoration: none;
                color: variables.$primary-color;
            }

            & i {
                padding-right: 1rem;
            }
        }
    }
}
</style>