<script>
export default {
    name: "SectionBlog"
}
</script>

<template>
    <section id="blog">
        <div class="container-lg bg-white text-center rounded-top ms_content">
            <h2 class="py-5 fs-2 fw-semibold">Latest News</h2>
            <div class="row">
                <div class="col-6">
                    <div class="card border-0 bg-none">
                        <img src="/blog-car.jpg" alt="foto news">
                        <div class="card-body">
                            <h4>What car to Start With?</h4>
                            <div>
                                February 7th, 2019 |
                                <span> 0 Comments </span>
                            </div>
                            <p>Lorem ipsum dolor sit amet, consectetur adipiscing</p>
                        </div>
                    </div>
                </div>
                <div class="col-6">
                    <div class="card border-0 bg-none">
                        <img src="/blog-post.jpg" class="card-img-top rounded-0" alt="foto news">
                        <div class="card-body">
                            <h4>Avada Driving School Expanding</h4>
                            <div>
                                February 7th, 2019 |
                                <span> 0 Comments </span>
                            </div>
                            <p>Lorem ipsum dolor sit amet, consectetur adipiscing</p>
                        </div>
                    </div>
                </div>
            </div>
            <a href="#">
                MORE FROM THE BLOG
            </a>
            <img class="ms_plus" src="/bg-plus.png" alt="stile del div">
        </div>

    </section>
</template>

<style lang="scss" scoped>
@use '../styles/partials/variables';
@use '../styles/partials/mixins';

#blog {
    background-image: url(/blog-bg.jpg);
    background-size: cover;
    background-position: bottom;
    padding-bottom: 150px;

    & .ms_content {
        border-top: 5px solid variables.$extra-color3;
        position: relative;
        top: -50px;
        padding-bottom: 20px;

        & h2 {
            color: variables.$color-dark-grey;
        }

        & .ms_plus {
            position: absolute;
            left: 0;
            bottom: -100px;
            width: 100%;
            height: 100px;
        }

        & a {
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
    }

    & .card {
        margin-bottom: 20px;

        & h4 {
            color: variables.$primary-color;
        }

        & div {
            font-size: 14px;
            padding-bottom: 20px;
            color: variables.$color-grey;

            & span {
                color: variables.$primary-color;

                &:hover {
                    color: lighten(variables.$primary-color, 10);
                    text-decoration: underline;
                    cursor: pointer;
                }
            }
        }

        & p {
            color: variables.$color-grey;
        }
    }
}
</style>