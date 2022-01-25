<template>
    <div class="container footer">
        <p>CT UBT - Av. Jovita Fortaleza, 878, Parquelândia, Fortaleza - Ce, 60455-411</p>
        <a href="https://carlos-mesquita.herokuapp.com" class="dev" target="_blank">
        Desenvolvido por Carlos Mesquita
        </a>
    </div>
</template>
<script>
    export default {
        name: 'Footer',
        data() {
            return {

            }
        }
    }
</script>
<style scoped>

    @import url('https://fonts.googleapis.com/css2?family=Noto+Sans&display=swap');

    .container {
        background: rgb(255, 187, 0);
        padding: 30px;
        flex-direction: column;
    }

    .footer {
        margin-top: 0%;
        margin-bottom: 0%;
        color: black;
        font-style: oblique;
        font-family: 'Noto Sans', sans-serif;
    }

    .dev {
        font-family: monospace;
        font-size: 10px;
        text-decoration: none;
        font-style: oblique;
        color: rgb(46, 46, 46);
    }
</style>