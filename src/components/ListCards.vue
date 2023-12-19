<template lang="">
    <section id="cards-wrapper" class="container">
        <div class="row">
            <h2>Found {{cardsList.length}} cards</h2>
        </div>
        <div class="cards row">
            <CardElement v-for="card in cardsList" :key="card.id" :card="card"/>
        </div>
    </section>
</template>
<script>
import CardElement from './CardElement.vue';
import axios from 'axios';
export default {
    data() {
        return {
            cardsList: [],
            apiUrl: 'https://db.ygoprodeck.com/api/v7/cardinfo.php?num=20&offset=0'
        }
    },
    components: {
        CardElement
    },
    methods: {
        getCards() {
            axios.get(this.apiUrl)
                .then((response) => {
                    // handle success
                    console.log(response);
                    this.cardsList = response.data.data;
                })
                .catch(function (error) {
                    // handle error
                    console.log(error);
                });
                
        }
    },
    created() {
        this.getCards();
    },
}
</script>
<style lang="scss" scoped>
@use '../styles/partials/variables.scss' as *;

#cards-wrapper {
    background-color: white;
    padding: 4rem;

    h2 {
        background-color: $dark-bg-colour;
        color: white;
    }
}
</style>