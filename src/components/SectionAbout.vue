<script>
export default {
    name: "SectionAbout",
    props: {
        instructors: Array
    }
}
</script>

<template>
    <section id="about">
        <div class="container-lg">
            <div class="row">
                <div class="col-8 pt-5">
                    <h2>
                        Your Instructors
                    </h2>
                    <p class="pt-3">
                        Lorem ipsum dolor sit amet, consectetur adipiscing elit. Nunc ultrices auctor
                        sapien id cursus. Aliquam maximus turpis in vehicula semper.
                    </p>
                </div>
                <div class="col-4">
                    <a href="#" class="ms_more-info">
                        MORE ABOUT US
                    </a>
                </div>
            </div>
        </div>
        <div class="container-lg">
            <div class="row">
                <div class="ms_box col-4" v-for="(person, index) in instructors" :key="index">
                    <div class="ms_rate">
                        <div class="card border-0">
                            <img :src="person.img" class="card-img-top" :alt="'foto di ' + person.name"
                                :title="'Instructor ' + person.name">
                            <div class="card-body">
                                <h3>
                                    {{ person.name }}
                                </h3>
                                <ul class="py-1">
                                    <li class="pe-4" v-for="(element, i) in person.social" :key="i">
                                        <a :href="element.href">
                                            <i :class="element.icon"></i>
                                        </a>
                                    </li>
                                </ul>
                                <p>
                                    {{ person.description }}
                                </p>
                            </div>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </section>
</template>

<style lang="scss" scoped>
@use '../styles/partials/variables';
@use '../styles/partials/mixins';

.col-8 h2 {
    color: variables.$color-dark-grey;
    font-size: 36px;
    font-weight: bold;
}

.col-8 p {
    color: variables.$color-grey;
    line-height: 2rem;
    font-size: 18px;
}

.col-4 {
    @include mixins.d-flex-center;

    & .ms_more-info {
        @include mixins.button;
        background-color: variables.$primary-color;
        text-decoration: none;
        width: 100%;
        text-align: center;
        font-weight: 600;

        &:hover {
            background-color: lighten(variables.$primary-color, 10);
        }

        &:active {
            background-color: darken(variables.$primary-color, 10);
        }
    }
}

.ms_box {
    margin: 3rem 0;
    position: relative;
    bottom: -80px;

    & .ms_rate {
        height: 100%;
        width: 100%;
        border-radius: 10px;
        border-top: 6px solid variables.$primary-color;
        box-shadow: 0px 0px 2px 2px variables.$color-light-grey;
        background-color: variables.$color-white;
        padding: 2rem 0;

        &:hover {
            transform: scale(1.1);
        }

        & .card {
            width: 80%;
            margin: auto;
            text-align: center;

            & .card-body {

                & h3 {
                    font-weight: bold;
                }

                & p {
                    color: variables.$color-grey;
                }

                & ul li {
                    display: inline-block;
                    list-style: none;

                    & a {
                        text-decoration: none;
                        color: variables.$color-grey;
                    }
                }
            }
        }
    }
}
</style>