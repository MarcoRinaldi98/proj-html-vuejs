<script>
export default {
    name: "FooterBottom"
}
</script>

<template>
    <section id="footer-bottom">
        <div class="container-sm">
            <div>
                © Copyright 2012 - 2020 | Avada Theme by
                <span> ThemeFusion </span>
                | All Rights Reserved | Powered by
                <span> WordPress </span>
            </div>
            <ul>
                <li>
                    <a href="#">
                        <i class="fa-brands fa-facebook-f"></i>
                    </a>
                </li>
                <li>
                    <a href="#">
                        <i class="fa-brands fa-twitter"></i>
                    </a>
                </li>
                <li>
                    <a href="#">
                        <i class="fa-brands fa-youtube"></i>
                    </a>
                </li>
                <li>
                    <a href="#">
                        <i class="fa-brands fa-instagram"></i>
                    </a>
                </li>
            </ul>
        </div>
    </section>
</template>

<style lang="scss" scoped>
@use '../styles/partials/variables';
@use '../styles/partials/mixins';

#footer-bottom {
    height: 100px;
    background-color: variables.$secondary-color;

    & .container-sm {
        @include mixins.d-flex-between;
        height: 100%;

        & div {
            color: variables.$extra-color7;

            & span {
                color: variables.$primary-color;
            }
        }

        & ul li {
            display: inline-block;
            padding-left: 1rem;

            & a {
                text-decoration: none;
                color: variables.$color-white;
            }
        }
    }
}
</style>