<script>
export default {
    name: "SectionTestimonials",
    props: {
        testimonials: Array
    }
}
</script>

<template>
    <section id="testimonials">
        <div class="ms_container">
            <div class="ms_slider text-center">
                <h2>Testimonials</h2>
                <p>Here's what our happy drivers had to say about our services:</p>

                <div class="ms_image-list">
                    <img src="/testimonial-sophia.png" alt="foto di sophia">
                </div>

                <p>Avado D'iving School really helped build my confidence behind the wheel and with driving in generon ond
                    they got me a first time poss! Highly recammended.</p>

                <h5>Sophia Jones</h5>

                <div class="ms_indicators">
                    <span class="ms_point ms_active">

                    </span>
                    <span class="ms_point">

                    </span>
                    <span class="ms_point">

                    </span>
                    <span class="ms_point">

                    </span>
                    <span class="ms_point">

                    </span>
                </div>
            </div>
        </div>
    </section>
</template>

<style lang="scss" scoped>
@use '../styles/partials/variables';
@use '../styles/partials/mixins';

#testimonials {
    background-image: url(/testimonial-bg.jpg);
    background-size: cover;
    background-position: bottom;
    padding: 100px 0;

    & .ms_container {
        max-width: 900px;
        margin: auto;

        & .ms_slider {
            padding: 2rem;

            & h2 {
                font-size: 40px;
                font-weight: bold;
                color: variables.$color-dark-grey;
            }

            & p {
                color: variables.$color-grey;
                line-height: 2rem;
                padding: 0 3rem;
            }

            & h5 {
                font-size: 18px;
                font-weight: bold;
                padding: 2rem 0;
                color: variables.$color-grey;
            }

            & .ms_image-list {
                width: 200px;
                height: 200px;
                margin: 2rem auto;


                & img {
                    height: 100%;
                    width: 100%;
                }
            }

            & .ms_indicators {
                margin: auto;

                & .ms_point {
                    display: inline-block;
                    height: 10px;
                    width: 10px;
                    border-radius: 50%;
                    border: 1px solid variables.$color-grey;
                    margin-right: 10px;
                }
            }
        }
    }
}

.ms_active {
    background-color: variables.$color-grey;
}
</style>