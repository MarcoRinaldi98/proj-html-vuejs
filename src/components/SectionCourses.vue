<script>
export default {
    name: "SectionCourses",
    props: {
        type: Array
    }
}
</script>

<template>
    <section id="courses">
        <div class="container-lg">
            <div class="row">
                <div class="col-6">
                    <div class="ms_new">
                        <h2 class="fw-semibold">
                            Courses
                        </h2>
                        <p class="py-5">
                            Lorem ipsum dolor sit amet. consectetur
                            adipiscing elit. Nunc ultrices auctor sapien id
                            cursus. Aliquom maximus turpis in vehiculo
                            semper.
                        </p>
                        <a href="#">
                            COURSE INFORMATION
                        </a>
                    </div>
                </div>
                <div class="col-2 mt-5" v-for="(element, index) in type" :key="index">
                    <div class="card bg-transparent border-0">
                        <img :src="element.image" :alt="'foto del corso di ' + element.name">
                        <div class="card-body">
                            <h3>{{ element.name }}</h3>
                            <a href="#">LEARN MORE</a>
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

#courses {
    background-image: url(/bg-courses.jpg);
    background-size: cover;
    background-position: bottom;
}

.ms_new {
    margin: 0;
    background-image: url(/new-corner.jpg);
    background-repeat: no-repeat;
    background-position: top left;
    text-align: center;
    background-color: variables.$color-white;
    padding: 6rem 2rem;
    border-radius: 10px;
    box-shadow: 0px 0px 4px variables.$color-light-grey;
    position: relative;
    top: -20px;

    & h2 {
        font-size: 34px;
        color: variables.$color-dark-grey;
    }

    & p {
        line-height: 2rem;
        color: variables.$color-grey;
    }

    & a {
        text-decoration: none;
        @include mixins.button;

        &:hover {
            background-color: lighten(variables.$primary-color, 10);
        }

        &:active {
            background-color: darken(variables.$primary-color, 10);
        }
    }
}



.card-body {
    text-align: center;

    & h3 {
        font-size: 16px;
        font-weight: bold;
        color: variables.$extra-color3;
        padding: 1.5rem 0;
    }

    & a {
        @include mixins.button2;
        text-decoration: none;
        font-size: 12px;

        &:hover {
            color: variables.$primary-color;
            border: 4px solid variables.$primary-color;
        }


    }
}

/* MEDIA QUERY */
@media screen and (max-width: 1200px) {
    .card {
        margin-top: 100px;
    }

    .card-body a {
        display: none;
    }
}
</style>