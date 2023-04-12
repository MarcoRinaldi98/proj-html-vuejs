<script>
export default {
    name: "SectionContactUs"
}
</script>

<template>
    <section id="contact-us">
        <div class="container-sm d-flex justify-content-between align-items-center h-100">
            <div class="text-white">
                <h1 class="pb-2">Start Learning to Drive Today</h1>
                <h4>Give us a call to schedule your frist driving lesson</h4>
            </div>
            <div class="fs-1 text-white">
                <i class="pe-3 fa-solid fa-phone-flip"></i>
                1-800-555-555
            </div>
        </div>
    </section>
</template>

<style lang="scss" scoped>
@use '../styles/partials/variables';
@use '../styles/partials/mixins';

#contact-us {
    height: 300px;
    background-image: url(/bg-contact-us.jpg);
    background-size: cover;
    background-position: center;

    & h1 {
        font-weight: 600;
    }
}
</style>