<script>
export default {
    name: "SectionRate"
}
</script>

<template>
    <section id="rate">
        <div class="container-sm">
            <div class="row">
                <div class="ms_box col-4">
                    <div class="ms_rate">
                        <div class="ms_progress" style="--progress: 345deg;">
                            <span>
                                95%
                            </span>
                        </div>
                        <div class="ms_type-rate">
                            PASS RATE
                        </div>
                    </div>
                </div>
                <div class="ms_box col-4">
                    <div class="ms_rate">
                        <div class="ms_progress" style="--progress: 360deg;">
                            <span>
                                100%
                            </span>
                        </div>
                        <div class="ms_type-rate">
                            REFERRAL RATE
                        </div>
                    </div>
                </div>
                <div class="ms_box col-4">
                    <div class="ms_rate">
                        <div class="ms_progress" style="--progress: 3deg;">
                            <span>
                                0%
                            </span>
                        </div>
                        <div class="ms_type-rate">
                            ACCIDENT RATE
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

#rate {
    position: relative;

    &:before {
        content: ' ';
        display: block;
        position: absolute;
        left: 0;
        top: 0;
        width: 100%;
        height: 100%;
        filter: contrast(80%);
        background-image: url(/bg-plus.png);
        background-repeat: no-repeat;
        background-size: contain;
    }

    & .container-sm {
        position: relative;

        & .ms_box {
            margin: 3rem 0;

            & .ms_rate {
                height: 100%;
                width: 100%;
                border-radius: 10px;
                border-top: 6px solid variables.$primary-alternative-color;
                box-shadow: 0px 10px 10px variables.$extra-color7;
                background-color: variables.$color-white;
                padding: 2rem 0;

                & .ms_progress {
                    margin: 20px auto;
                    display: flex;
                    width: 300px;
                    height: 300px;
                    border-radius: 50%;
                    background: conic-gradient(variables.$primary-alternative-color var(--progress), variables.$extra-color7 0deg);
                    font-size: 0;
                    position: relative;

                    &::after {
                        content: '';
                        display: flex;
                        justify-content: center;
                        flex-direction: column;
                        width: 100%;
                        margin: 10px;
                        border-radius: 50%;
                        background: white;
                        font-size: 1rem;
                        text-align: center;
                    }

                    & span {
                        position: absolute;
                        top: 50%;
                        left: 50%;
                        transform: translate(-50%, -50%);
                        font-size: 50px;
                        color: variables.$secondary-alternative-color;
                    }
                }

                & .ms_type-rate {
                    color: variables.$secondary-alternative-color;
                    text-align: center;
                    font-weight: 500;
                    font-size: 20px;
                    padding-top: 2rem;
                }
            }
        }
    }
}
</style>