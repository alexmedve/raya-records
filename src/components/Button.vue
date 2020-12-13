<template>
    <div class="app-button">
        <div class="text"> 
            {{text}}
        </div>
    </div>
</template>

<script>
    export default {
        props: {
            text: {
                default: '',
                type: String
            }
        }
    }
</script>

<style lang="scss">
    .app-button {
        height: 8rem;
        width: 100%;
        max-width: 40rem;
        cursor: pointer;
        border: 2px solid $color-white;
        color: $color-white;
        @include flex-center;
        font-size: 2.5rem;
        font-family: $font-text;
        letter-spacing: 0.2rem;
        position: relative;
        overflow: hidden;

        &__text {
            width: auto;
            height: auto;
            display: block;
            z-index: 1;
        }

        &::before {
            content: "";
            position: absolute;
            width: 100%;
            height: 100%;
            top: 0;
            left: 0;
            z-index: 0;
            background-image: url("../assets/img/spiral.png");
            background-size: cover;
        }
    }
</style>