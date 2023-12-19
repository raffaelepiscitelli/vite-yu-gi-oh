<template lang="">
    <article>
        <section class="img">
            <img :src="card.card_images[0].image_url" alt="">
        </section>
        <h3>{{card.name}}</h3>
        <p>{{card.archetype}}</p>
    </article>
</template>
<script>
export default {
    props: {
        card: {
            type: Object,
            required: true,
        }
    }
}
</script>
<style lang="scss" scoped>
@use '../styles/partials/variables.scss' as *;
    article {
        width: calc(100% / 5 - 1rem);
        margin: 0 0.5rem;
        margin-bottom: 1rem;
        background-color: $bg-colour;
        text-align: center;
            h3 {
                text-transform: uppercase;
                color: white;
                font-size: 1.2rem;
                font-weight: bolder;
                margin-top: 1rem;
            }
            img {
                width: 100%;
                height: 100%;
            }
    }
</style>