<template>
    <div class="mapa">
    <h2>Nossa localização</h2>

    <button class="botaoSub" @click="mostrarMapa" >Clique aqui</button>

    <iframe v-show="mostrar_mapa" src="https://www.google.com/maps/embed?pb=!1m18!1m12!1m3!1d3981.326656121505!2d-38.55400328524104!3d-3.738819797279845!2m3!1f0!2f0!3f0!3m2!1i1024!2i768!4f13.1!3m3!1m2!1s0x7c749722defc031%3A0x23d3119c9c49abfc!2sCT%20UBT!5e0!3m2!1spt-BR!2sbr!4v1643119109290!5m2!1spt-BR!2sbr" width="400" height="300" style="border:0;" allowfullscreen="" loading="lazy"></iframe>

    </div>
    
</template>

<script>
    

    export default {
        name:'Localizacao',
        data() {
            return {
                mostrar_mapa: false,
            }
        },
        methods: {
            mostrarMapa(e) {
                this.mostrar_mapa = !this.mostrar_mapa;
            }
        }
    }
</script>

<style scoped>
    h2 {
        color: white;
    }


    .botaoSub {
        background: rgb(255, 187, 0);
        padding: 8px;
        color: rgb(255, 255, 255);
        text-shadow: 1px 1px 1px rgb(0, 0, 0);
        border-radius: 5px;
        border: none;
        margin: auto;
        margin-bottom: 1%;
        
    }
    .mapa {
        display: flex;
        justify-content: space-evenly;
        margin-top: 4%;
        background: black;
        flex-direction: column;
        align-items: center;
        
    }

    iframe {
        margin-top: 1%;
        margin-bottom: 2%;
    }
</style>