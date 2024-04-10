<template>
    <div class="col-12 col-md-4">
        <h5>{{ title }}</h5>
        <ul>
            <li v-for="(item, index) in items" :key="index">
                <a :href="item.url">{{ item.name }}</a>
            </li>
        </ul>
    </div>
</template>

<script>
    export default {
        name: 'MenuComponent',
        props: ['title', 'items']
        
    }
</script>

<style lang="scss" scoped>
    @use '../assets/styles/partials/variables' as *;

    h5{
        color: $contentherecolor;
    }

    ul{
        list-style: none;
        margin: 20px -30px;

        li{

            a{
                text-decoration: none;
                color: black;
            }
        }
    }
</style>