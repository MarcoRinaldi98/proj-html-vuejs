<script>
export default {
    name: "HeaderTop"
}
</script>

<template>
    <section id="header-top">
        <div class="container-lg h-100 w-100">
            <span>
                We have a 95% Successful Pass Rate!
            </span>
            <span>
                <i class="fa-solid fa-phone-flip"></i>
                Give us a call to book your tuition! 1-800-555-555
            </span>
        </div>
    </section>
</template>

<style lang="scss" scoped>
@use '../styles/partials/variables';
@use '../styles/partials/mixins';

#header-top {
    background-color: variables.$secondary-color;
    height: 30px;

    & div {
        @include mixins.d-flex-between;

        & span {
            color: variables.$color-grey;
            font-size: 14px;
        }
    }
}
</style>