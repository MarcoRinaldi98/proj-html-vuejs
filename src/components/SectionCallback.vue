<script>
export default {
    name: "SectionCallback"
}
</script>

<template>
    <section id="callback" class="pb-5">
        <div class="container-sm">
            <div class="row">
                <div class="ms_col-left col-6">
                    <h2 class="fw-semibold">
                        Get Behind The Wheel
                    </h2>
                    <h6>
                        Corem ipsum dolor sit amet. consectetur adipiscing elit.
                        Nunc ultrices auctor sapien id cursus. Aliquam maximus
                        turpis in vehicula semper.
                    </h6>
                    <p>
                        Lorem ipsum dolor sit amet, consectetur adipiscing elit. Nunc ultrices
                        auctor sapien id cursus. Aliquam maximus turpis in vehicula semper.
                        Fusce et ultrices libero. at suscipit lacus, Sed vitae fringilla nibh. Nunc
                        ultrices auctor sapien id cursus, Aliquam maximus turpis in vehicula
                        semper, Fusce et ultrices libero. at suscipit lacus. Sed vitae fringilla nibh.
                    </p>
                </div>
                <div class="ms_col-right col-6 text-center">
                    <div class="ms_form">
                        <h3>Frist Lesson Free!</h3>
                        <p class="py-3">When you make a block booking with us your frist lesson is included free.</p>
                        <form>
                            <div class="input-group mb-3">
                                <input type="text" class="form-control border-end-0" placeholder="Your Name*" required>
                                <span class="input-group-text border-start-0">
                                    <img src="/form-name.png" alt="icona form">
                                </span>
                            </div>
                            <div class="mb-3">
                                <input type="email" class="form-control" placeholder="Email*" required>
                            </div>
                            <div class="mb-3">
                                <input type="text" class="form-control" placeholder="Telephone">
                            </div>
                            <div class="mb-3">
                                <input type="text" class="form-control" placeholder="Location">
                            </div>
                            <div class="mb-3">
                                <button class="fw-semibold my-3">REQUEST A CALLBACK</button>
                            </div>
                        </form>
                    </div>
                </div>
            </div>
        </div>
    </section>
</template>

<style lang="scss" scoped>
@use '../styles/partials/variables';
@use '../styles/partials/mixins';

.ms_col-left {
    margin: auto;

    & h2 {
        padding-top: 20px;
        font-size: 32px;
        color: variables.$color-dark-grey;
    }

    & h6 {
        padding: 1.5rem 0;
        color: variables.$color-grey;
        line-height: 2rem;
        padding-right: 2rem;
        font-size: 18px;
    }

    & p {
        font-size: 14px;
        color: variables.$color-grey;
        line-height: 1.5rem;
        padding-right: 2rem;
        line-height: 2rem;
    }
}

.ms_col-right {

    & .ms_form {
        background-color: variables.$color-white;
        box-shadow: 0px 0px 5px 5px variables.$color-light-grey;
        padding: 2rem;
        border-radius: 10px;
        width: 80%;
        margin: auto;
        position: relative;
        top: -20px;

        & h3 {
            color: variables.$primary-color;
        }

        & p {
            font-size: 14px;
            color: variables.$color-grey;
            line-height: 1.5rem;
        }

        & form div input {
            background-color: variables.$color-light-grey;
        }

        & form div span {
            background-color: variables.$color-light-grey;
        }

        & form div button {
            @include mixins.button;
            border: none;
            background-color: variables.$primary-color;

            &:hover {
                background-color: lighten(variables.$primary-color, 10);
            }

            &:active {
                background-color: darken(variables.$primary-color, 10);
            }
        }
    }
}
</style>