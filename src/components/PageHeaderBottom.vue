<script>
export default {
    name: "PageHeaderBottom",
    props: {
        nav: Array
    }
}
</script>

<template>
    <section class="ms_header-bottom">
        <nav class="container-sm">
            <div class="ms_brand">
                <a href="#">
                    <img src="/logo-avada.png" alt="Logo Avada Driving School" />
                </a>
            </div>
            <ul>
                <li v-for="(link, i) in nav" :key="i">
                    <a class="ms_nav-link" :href="link.href">
                        {{ link.text }}
                    </a>
                </li>
                <li>
                    <a class="ms_button" href="#">
                        BOOK NOW
                    </a>
                </li>
            </ul>
        </nav>
    </section>
</template>

<style lang="scss" scoped>
@use '../styles/partials/variables';
@use '../styles/partials/mixins';



.ms_header-bottom {
    height: 90px;
    background-color: rgba($color: variables.$secondary-color, $alpha: 0.7);

    & nav {
        @include mixins.d-flex-between;
        height: 100%;

        & .ms_brand img {
            height: 50px
        }

        & ul {
            height: 100%;
            margin: 0;

            & li {
                display: inline-block;
                line-height: 90px;
                margin: 0 1rem;

                & .ms_nav-link {
                    text-decoration: none;
                    text-transform: uppercase;
                    font-size: 14px;
                    font-weight: bold;
                    color: variables.$color-white;
                    padding-bottom: 1rem;
                }

                &:hover .ms_nav-link {
                    border-bottom: 2px solid variables.$primary-color;
                    color: variables.$primary-color;
                }

                &:nth-child(4)::after {
                    content: 'new';
                    margin-left: 0.5rem;
                    padding: 2px 4px;
                    border-radius: 5px;
                    color: variables.$color-white;
                    font-size: 12px;
                    background-color: variables.$primary-color;
                }

                & .ms_button {
                    @include mixins.button;
                    text-decoration: none;
                    font-weight: bold;
                    font-size: 14px;
                }


            }
        }
    }
}
</style>