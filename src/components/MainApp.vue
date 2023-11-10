<template>
    <main>
        <section class="container">
            <div class="row gy-2">
                <div class="col-12 col-md-4 col-lg-3" v-for="(pasta, index) in pastas" :key="index">
                    <CardComponent :image="pasta.src" :title="pasta.titolo" />
                </div>

            </div>
        </section>


    </main>
</template>

<script>
import { products } from '../data/product.js';
import CardComponent from './CardComponent.vue';

export default {
    name: 'MainApp',
    comnponents: {
        CardComponent
    },
    data() {
        return {
            pastas: products
        };
    },
    components: { CardComponent }
}
</script>

<style lang="scss" scoped>
@use '../assets/styles/partials/variables' as *;

main {
    background-image: url('/images/fondo-pag-speciali.jpg');
    text-align: center;
    padding: 20px;

    h1 {
        color: black;
    }
}
</style>