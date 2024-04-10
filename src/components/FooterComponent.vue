<template>
    <footer>
        <div class="container">
            <div class="row">
                <div class="col-12 col-md-4">
                    <img src="../assets/img/la-molisana-logo.png" alt="logo la molisana">
                </div>
                <MenuComponent title="PASTIFICIO" :items="links.pastificio" />
                <MenuComponent title="PRODOTTI" :items="links.prodotti" />
            </div>
        </div> 
    </footer>
</template>

<script>
    import MenuComponent from './MenuComponent.vue';
    export default {
        name: 'FooterComponent',
        components: {
            MenuComponent
        },
        data() {
            return {
                links: {
                    pastificio: [
                        {
                            name: 'Il Pastificio',
                            url: '#'
                        },
                        {
                            name: 'Grano',
                            url: '#'
                        },
                        {
                            name: 'Filiera',
                            url: '#'
                        },
                        {
                            name: '100 anni di pasta',
                            url: '#'
                        },
                        {
                            name: 'Sartoria della pasta',
                            url: '#'
                        }
                    ],
                    prodotti: [
                        {
                            name: 'Le Classiche',
                            url: '#'
                        },
                        {
                            name: 'Le Integrali',
                            url: '#'
                        },
                        {
                            name: 'Le Speciali',
                            url: '#'
                        },
                        {
                            name: 'Le Biologiche',
                            url: '#'
                        },
                        {
                            name: 'Le Gluten-Free',
                            url: '#'
                        } 
                    ]
                }
                
                
            }
        },
    }
</script>

<style lang="scss" scoped>
    footer{
        background-image: url('../assets/img/footer-montagne-bottom.jpg');
        background-position: bottom;
        background-repeat: no-repeat;
    }
</style>