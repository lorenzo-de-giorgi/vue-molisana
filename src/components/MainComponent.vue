<template>
    <main>
        <div class="container">
            <h2>Lista Prodotti</h2>
            <div class="row">
                <div class="col-12 col-md-6 col-lg-3 mb-4" v-for="(item, index) in products" :key="index">
                    <CardComponent :image="item.src" :title="item.titolo" :text="`Tipo: ${item.tipo} - Cottura: ${item.cottura} min`" />
                </div>
            </div>
        </div>
    </main>
</template>

<script>
    import { prodotti } from '../data/store.js';
    import CardComponent from '../components/CardComponent.vue';
    export default {
        name: 'MainComponent',
        components: {
            CardComponent
        },
        data() {
            return {
                products: prodotti,
            }
        },
        mounted() {
            console.log(this.products)
        },
    }
</script>

<style lang="scss" scoped>
    @use '../assets/styles/partials/variables' as *;
    main{
        background-image: url('../assets/img/fondo-pag-speciali.jpg');
    }

    h2{
        padding: 40px;
        color: $contentherecolor;
        text-align: center;
    }
</style>