<template>
    <div class="container">
        <img :src="carro" alt="Imagem Carro">
        <h3 class="title">{{ title }}</h3>
        <div class="btns">
            <button class="btn cotacao">Cotação</button>
            <button class="btn ligar">Ligar</button>
        </div>
        <div class="social">
            <p>Compartilhe:</p>
            <img class="icon face" src="@/assets/facebook.svg" alt="icone whatsapp">
            <img class="icon wpp" src="@/assets/whatsapp.svg" alt="icone whatsapp">
        </div>
    </div>
</template>
<script>
export default {
    name: 'cardComponent',
    props: {
        carro: String,
        title: String
    },
    data() {
        return {

        }
    },
    methods:{
    }
}
</script>
<style scoped>

img {
  max-width: 100%;
  height: auto;
}
.title{
    text-align: start;
    margin-left: 10px;
    font-weight: normal;
    font-size: 20px;
    color: #262626;
}
.face, .wpp{
    width: 20px;
    margin: 20px 8px 20px 8px;
}

.btns{
    display: flex;
    justify-content: space-around;
}
.btn{
    border-style: none;
    padding: 10px 65px 10px 65px;
    color: #fff;
}
.cotacao{
    background-color: #1C69D4;
}
.cotacao:hover{
    cursor: pointer;
    background-color: #0351BE;
}
.ligar{
    background-color: #000000;
}
.ligar:hover{
    cursor: pointer;
    background-color: #575757;
}
.social{
    display: flex;
    align-items: center;
    margin-left: 10px;
}
.social p{
    color: #666666;
    font-size: 12px;
}
@media(min-width: 765px){
    .ligar{
        display: none;
    }
    .cotacao{
        width: 100%;
    }
    .container{
        max-width: 315px;
    }
}
</style>