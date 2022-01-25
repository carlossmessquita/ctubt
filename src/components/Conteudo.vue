<template>
    <div class="hello">
        <h1>{{ msg }}</h1>

        <div class="container">
            <div class="conteudo">
                <h3>Modalidades e Horários</h3>
                <br>
                <button class="botao" @click="mostrarQuadro">Turmas e Horários</button>
                <iframe v-show="mostrar_quadro" src="https://drive.google.com/file/d/1PWkYZ4i3anUz7ZhV3Z9ZWvKhwWL9FFo6/preview"  width="240" height="480" allow="autoplay"></iframe>
                
            </div>

            <div class="conteudo">
                <h3>Conheça nossos planos</h3>
                <br>
                <a class="botao" href="https://planos.ctubt.com.br/" target="_blank" rel="noopener">Planos</a>
            </div>
            
            <div class="conteudo">
                <h3>Quer treinar com a gente?</h3>
                <br>
                <a class="botao" href="https://api.whatsapp.com/send?phone=558588276380" target="_blank" rel="noopener">Chama aqui</a>
            </div>

            <div class="conteudo">
                <h3>Segue a gente no insta também</h3>
                <br>
                <a class="botao" href="https://www.instagram.com/ctubt/" target="_blank" rel="noopener">@ctubt</a>
            </div>
        </div>
        <Localizacao />
        <Footer />
    </div>
</template>

<script>
    import Localizacao from './Localizacao.vue';
    import Footer from './Footer.vue';
    export default {
        name: 'Conteudo',
        components: {
            Localizacao,
            Footer
        },
        props: ['msg'],
        data() {
            return {
                mostrar_quadro: false
                
            }
        },
        methods: {
            mostrarQuadro() {
                this.mostrar_quadro = !this.mostrar_quadro;
            }
        }

    }
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
    h1 {
        background: rgb(255, 187, 0); 
        padding: 5px;
        color: black;  
    }

    h3 {
        margin: 40px 0 0;
        color: white;

    }
    
    p {
        background: rgb(0, 0, 0); 
        padding: 2px;
        color: white;
    }

    a {
        text-decoration: none;
        font-family: monospace;
        font-weight: bolder;
        font-size: 15px;
        
    }

    .botao {
        background: rgb(255, 187, 0);
        padding: 8px;
        color: rgb(255, 255, 255);
        text-shadow: 1px 1px 1px rgb(0, 0, 0);
        border-radius: 5px;
        border: none;
        margin-bottom: 3%;
        
    }

    .container {
        display: flex;
        justify-content: space-evenly;
        
    }

    .conteudo {
        align-items: center;
        background: rgba(0, 0, 0, 0.884);
        padding: 5px;
        margin: 2%;
        border-radius: 5px;


    }

    @media only screen and (max-width: 600px) {
        .container {
            flex-direction: column;
        }
    }
</style>
