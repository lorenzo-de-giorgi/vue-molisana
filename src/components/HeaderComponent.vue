<template>
    <header class="container text-center">
        <img src="../assets/img/la-molisana-logo.png" alt="la molisana logo">
        <ul>
            <li v-for="(item, index) in menu" :key="index">
                <a :href="item.url">{{ item.name }}</a>
            </li>
        </ul>
    </header>
</template>

<script>
    export default {
        name: 'HeaderComponent',
        data() {
            return {
                menu: [
                    {
                        name: 'Home',
                        ul: '#'
                    },
                    {
                        name: 'Prodotti',
                        ul: '#'
                    },
                    {
                        name: 'Chi Siamo',
                        ul: '#'
                    },
                    {
                        name: 'Contatti',
                        ul: '#'
                    }
                ]
            }
        },
    }
</script>

<style lang="scss" scoped>
    @use '../assets/styles/partials/variables' as *;
    ul{
        list-style: none;
        margin: 20px 0;
        display: flex;
        justify-content: center;

        li{
            margin: 0 10px;

            a{
                padding: 6px 10px;
                text-decoration: none;
                color: black;

                &:hover{
                    background-color: $menuhover;
                }
            }
        }
    }
</style>