<template>
    <main>
        <div class="container">
        <h2>--> Content goes here <--</h2>
        </div>
    </main>
</template>

<script>
    export default {
        name: 'MainComponent'
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