<template>
    <div class="searche">
        <input
                id="searche"
                class="searche__input"
                type="text"
                placeholder="Searche..."
        />
    </div>
</template>

<script>
    export default {
        name: "SearcheComponent",
        data() {
            return {};
        },
    };
</script>

<style lang="scss">
    @import "../../variables";
    .searche {
        position: relative;
        width: 100%;
        display: flex;
        align-items: center;
        order: 1;
        @include mq($from: tablet) {
            order: 0;
            width: unset;
        }
        @include mq($until: tablet) {
            margin-top: 20px;
        }
        &__input {
            width: 100%;
            height: 44px;
            padding: 0 15px;
            max-width: unset;
            background: #fff;
            border: 2px solid $color-grey-border;
            border-radius: 5px;
            font-size: 16px;
            line-height: 54px;
            color: #000;
            @include mq($from: desktop) {
                width: 40vw;
                height: 54px;
                max-width: 800px;
            }
        }
        &::after {
            content: url("../../assets/ico/search-svgrepo-com.svg");
            position: absolute;
            width: 25px;
            height: 25px;
            right: 8px;
        }
    }
</style>
