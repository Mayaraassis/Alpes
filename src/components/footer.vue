<template>
    <div class="container">
        <p class="text">
            Lorem ipsum dolor sit amet, consectetur adipiscing elit.
            Sed a elementum orci, vitae commodo nibh. In vitae convallis nisl.
            Morbi rhoncus mattis purus sed commodo. Integer rhoncus ex risus.
            Proin efficitur elit nunc, ut pulvinar massa egestas in.
            Fusce quis quam viverra, pretium quam ac, consectetur lectus.
        </p>
        <hr>
        <div class="box_rodape">
            <img class="logo" src="@/assets/logo-bmw-rio.svg" alt="logo bmw">
            <p class="copy">© Copyright © 2021 Lorem ipsum dolor sit amet.</p>
            <div class="box">
                <p>Feito por: </p>
                <img class="alpes_logo" src="@/assets/logo-alpes.png" alt="logo alpes">
            </div>
        </div>
    </div>
</template>
<script>
export default {
    name: 'footerComponent',
    data() {
        return {

        }
    }
}
</script>
<style scoped>
.container {
    background-color: #E6E6E6;
    padding: 20px;
    text-align: center;
    color: #262626;
    display: flex;
    flex-direction: column;
    align-items: center;
    margin-bottom: 60px;
}

.text {
    font-size: 12px;
    margin-bottom: 30px;
    display: flex;
    justify-content: center;
    align-items: center;
    max-width: 1350px;

}

.copy {
    font-size: 12px;
}

.box {
    display: flex;
    justify-content: center;
    align-items: center;
    font-size: 12px;
}

.alpes_logo {
    margin-left: 10px;
}
.logo{
    display: none;
}

@media(min-width: 765px) {
    .box_rodape {
        width: 100%;
        display: flex;
        justify-content: space-around;
        align-items: center;
    }

    .logo {
        display: block;
        width: 34px;
        height: 34px;

    }
}
</style>