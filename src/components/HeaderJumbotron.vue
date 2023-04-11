<script>
export default {
    name: "HeaderJumbotron",
    props: {
        nav: Array
    }
}
</script>

<template>
    <section id="jumbotron">
        <div id="header-bottom">
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
        </div>
        <div class="ms_text container-sm">
            <h1>Drive with Avada</h1>
            <p class="py-2">We offer the finest driving tuition money can buy</p>
        </div>
        <div class="ms_try">
            <div class="ms_square">
                <i class="ms_number ms_color1 fa-solid fa-folder-closed"></i>
                <div class="ms_offert">Demos</div>
            </div>
            <div class="ms_square">
                <span class="ms_price">$ </span>
                <div class="ms_number ms_color2">39</div>
                <div class="ms_offert">On Sale</div>
            </div>
        </div>
    </section>
</template>

<style lang="scss" scoped>
@use '../styles/partials/variables';
@use '../styles/partials/mixins';

#jumbotron {
    background-image: url(/bg-hero.jpg);
    background-size: cover;
    height: 600px;
    width: 100%;
    position: relative;

    #header-bottom {
        position: absolute;
        top: 0;
        left: 0;
        width: 100%;
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

    & .ms_text {
        height: 100%;
        color: variables.$color-white;
        padding-top: 300px;
        letter-spacing: 1.5px;
    }

    & .ms_try {
        position: absolute;
        top: 80px;
        right: 15px;

        & .ms_square {
            height: 60px;
            width: 60px;
            background-color: variables.$extra-color7;
            cursor: pointer;
            border-radius: 5px;
            margin-bottom: 6px;
            position: relative;
            @include mixins.d-flex-around;
            flex-direction: column;
            box-shadow: 0px 0px 2px variables.$color-black;

            & .ms_price {
                font-size: 12px;
                color: variables.$primary-color;
                position: absolute;
                top: 5px;
                left: 5px;
            }

            & .ms_number {
                text-align: center;
                font-size: 30px;
                width: 100%;
            }

            & .ms_offert {
                font-size: 12px;
                width: 100%;
                text-align: center;
                font-weight: bold;
                color: variables.$color-black;
            }
        }
    }
}

.ms_color1 {
    color: variables.$color-black;
}

.ms_color2 {
    color: variables.$primary-color;
}
</style>