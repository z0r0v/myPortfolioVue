<template>
    <div class="sites-info-component">
        <div class="sites-info-component__item">
            <a href="#">
                <figure>
                    <picture v-lazy-container="{ selector: 'img' }">
                        <source media="(max-width: 768px)" srcset="@/assets/img/vue.png">
                        <source srcset="@/assets/img/vue.png">
                        <img data-src="@/assets/img/vue.png" alt="html">
                    </picture>
                </figure>
                <p>
                    {{ms + vue}}
                </p>
            </a>
        </div>
        <div class="sites-info-component__item">
            <a href="#">
                <figure>
                    <picture v-lazy-container="{ selector: 'img' }">
                        <source media="(max-width: 768px)" srcset="@/assets/img/html5.png">
                        <source srcset="@/assets/img/html5.png">
                        <img data-src="@/assets/img/html5.png" alt="html">
                    </picture>
                </figure>
                <p>
                    {{ms + html}}
                </p>
            </a>
        </div>
        <div class="sites-info-component__item">
            <a href="#">
                <figure>
                    <picture v-lazy-container="{ selector: 'img' }">
                        <source media="(max-width: 768px)" srcset="@/assets/img/react.png">
                        <source srcset="@/assets/img/react.png">
                        <img data-src="@/assets/img/react.png" alt="html">
                    </picture>
                </figure>
                <p>
                    {{ms + react}}
                </p>
            </a>
        </div>

    </div>
</template>

<script>
    export default {
        name: "SitesInfoComponent",
        data() {
            return {
                ms: "My site on ",
                react: "react",
                vue: "vue",
                html: "html",

            };
        },
    }
</script>

<style lang="scss">
    @import "../../variables";
    .sites-info-component {
        display: flex;
        flex-wrap: wrap;
        margin: 20px 0;

        &__item {
            width: 50%;
            margin: 0 auto;
            display: flex;
            justify-content: center;
            align-items: center;
            @include mq($from: tablet) {
                width: calc(100% / 3);
            }
            figure picture img {
                width: 170px;
                height: 170px;
                opacity: 0.4;
            }
            p {
                text-align: center;
                color: $color-black;
                opacity: 0.4;
            }
        }

        &__item:hover {
            figure picture img {
                opacity: 1;
            }
            p {
                opacity: 1;
            }
        }
    }
</style>