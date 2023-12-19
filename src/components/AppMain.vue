<template lang="">
    <main>
        <ListCards/>
    </main>
</template>
<script>
import ListCards from './ListCards.vue';

export default {
    components: {
        ListCards
    }
}
</script>
<style lang="scss">
@use '../styles/partials/variables.scss' as *;

    main {
        background-color: $bg-colour;
    }
</style>