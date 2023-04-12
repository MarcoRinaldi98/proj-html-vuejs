<script>
export default {
    name: "SectionNewsletter"
}
</script>

<template>
    <section id="newsletter">
        <div class="ms_container">
            <h1 class="py-5">Sign up to our newsletter</h1>
            <form>
                <div class="mb-5">
                    <input type="email" class="form-control">
                </div>
                <div class="mb-3">
                    <button>SUBSCRIBE</button>
                </div>
            </form>
            <div class="pb-5">(We do not share your data with anybody, and only use it for its intended purpose)</div>
        </div>
    </section>
</template>

<style lang="scss" scoped>
@use '../styles/partials/variables';
@use '../styles/partials/mixins';

#newsletter {
    background-image: url(/newsletter-bg.jpg);
    background-size: cover;

    & .ms_container {
        max-width: 900px;
        margin: auto;
        padding: 50px 0;
        text-align: center;

        & h1 {
            font-weight: 500;
            color: variables.$color-dark-grey;
        }

        & form input {
            padding: 1rem;
            font-size: 20px;
        }

        & form button {
            width: 100%;
            @include mixins.button;
            background-color: variables.$primary-color;
            border: none;
            font-weight: 600;

            &:hover {
                background-color: lighten(variables.$primary-color, 10);
            }

            &:active {
                background-color: darken(variables.$primary-color, 10);
            }
        }

        & div {
            color: variables.$color-grey;
            font-size: 14px;
        }
    }
}
</style>