<template>
    <div class="hello">
        <h1>{{ msg }}</h1>

        <div class="container">
            <div class="conteudo">
                <h3>Modalidades e Horários</h3>               
                <br>
                <button class="botao" @click="mostrarQuadro">Turmas e Horários</button> 
            </div>

            <div v-show="mostrar_quadro" class="conteudo">
               <iframe  src="https://drive.google.com/file/d/1LX-4ZCtv_Agv9ETJBLrD0qxPK_i4xEMP/preview"    width="240" height="480" allow="autoplay"></iframe> 
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
                <h3>Produtos da Loja</h3>
                <br>
                <a class="botao" href="http://ctubt.kyte.site/" target="_blank" rel="noopener">Nossos Produtos</a>
            </div>

            <div class="conteudo">
                <h3>Nosso instagram</h3>
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

    @import url('https://fonts.googleapis.com/css2?family=Noto+Sans:wght@700&display=swap');
    h1 {
        background: rgb(255, 187, 0); 
        padding: 5px;
        color: black;  
        text-shadow: 1px 1px 1px linen;
        font-family: 'Noto Sans', sans-serif;
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
    
    button {
        font-family: monospace;
        font-weight: bolder;
    }

    .botao {
        background: rgb(255, 187, 0);
        padding: 8px;
        color: rgb(0, 0, 0);
        border-radius: 5px;
        border: none;
        margin-bottom: 3%;
        
    }

    .container {
        display: flex;
        justify-content: space-evenly;
        flex-wrap: wrap;
        
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

        iframe {
            width: 240px;
        }
    }
</style>
