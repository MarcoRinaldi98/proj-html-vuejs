<script>
export default {
    name: "FooterBottom",
    props: {
        social: Array
    }
}
</script>

<template>
    <section id="footer-bottom">
        <div class="ms_go-top rounded-top">
            <a href="#">
                <i class="p-3 text-white fa-solid fa-chevron-up"></i>
            </a>
        </div>
        <div class="container-lg">
            <div>
                © Copyright 2012 - 2020 | Avada Theme by
                <span> ThemeFusion </span>
                | All Rights Reserved | Powered by
                <span> WordPress </span>
            </div>
            <ul>
                <li v-for="(element, index) in social" :key="index">
                    <a href="#">
                        <i class="fa-brands" :class="element.name"></i>
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
    background-color: variables.$secondary-alternative-color;
    position: relative;

    & .ms_go-top {
        position: absolute;
        right: 120px;
        bottom: 0;
        width: 60px;
        height: 40px;
        background-color: variables.$secondary-color;
        @include mixins.d-flex-center;
    }

    & .container-lg {
        @include mixins.d-flex-between;
        height: 100%;

        & div {
            color: variables.$color-grey;

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