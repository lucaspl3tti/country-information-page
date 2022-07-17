<script>
import ToggleDarkmode from '@/components/ToggleDarkmode.vue';

export default {
    components: {
        ToggleDarkmode,
    }
};
</script>

<template>
    <header class="header">
        <div class="header__left">
            <div class="nav-heading">Where in the World</div>
        </div>

        <div class="header__right">
            <ToggleDarkmode />
        </div>
    </header>

    <div class="container">
        <RouterView />
    </div>
</template>

<style lang="scss">
@import '@/scss/abstracts/variables.scss';

.header {
    position: fixed;
    top: 0;
    display: flex;
    flex-flow: row nowrap;
    align-items: center;
    justify-content: space-between;
    width: 100vw;
    height: 80px;
    padding: 0 16px;
    background-color: $color-white;
    color: $color-black;
    box-shadow: 0 2px 4px 0 rgba($color: $color-black, $alpha: 0.1562);
    z-index: 1000;

    .nav-heading {
        font-size: 14px;
        font-weight: 700;
        line-height: 20px;
    }
}

.container {
    padding: 105px 16px 50px;
}

.app--darkmode {
    .header {
        background-color: $color-dark-secondary;
        color: $color-white;
    }
}

@media (min-width: 1200px) {
    .header {
        padding: 0 80px;

        .page-heading {
            font-size: 24px;
            font-weight: 800;
            line-height: 1;
        }
    }

    .container {
        padding: 125px 80px;
    }
}
</style>
