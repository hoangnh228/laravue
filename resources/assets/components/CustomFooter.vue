<template>
    <div id="footer">
        <div class="hr"></div>
        <div :class="containerClass">
            <p>
                <img src="/images/logo_grey.png" class="icon">
                <strong>Laravue</strong>. Full stack Laravel and Vue.js demo app
            </p>
        </div>
    </div>
</template>

<script>
    export default {
        computed: {
            containerClass() {
                return `${this.$route.name}-container`;
            }
        }
    }
</script>

<style>
    #footer {
        margin-bottom: 3em;
    }

    #footer .icon {
        height: 23px;
        display: inline-block;
        margin-bottom: -6px;
    }

    .hr {
        border-bottom: 1px solid #DBDBDB;
        margin: 3em 0;
    }

    #footer p {
        font-size: 15px;
        color: #767676 !important;
        display: flex;
    }

    #footer p img {
        padding-right: 6px;
    }
</style>
