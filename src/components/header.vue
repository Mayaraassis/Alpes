<template>
    <div class="container">
        <div class="header_mobile">
            <p class="box_tel">
                <img class="icon fone" src="@/assets/telefone.svg" alt="icone telefone">
                <a href="tel:2120424442">(21) 2042-4442</a>
            </p>
            <img class="logo" src="@/assets/logo-bmw-rio.svg" alt="logo bmw">
        </div>
        <div class="header_desktop">
            <div class="top">
                <div class="rets">
                    <p class="box_telefone ret">
                        <img class="icon fone" src="@/assets/telefone.svg" alt="icone telefone">
                        <a href="tel:2120424442">(21) 2042-4442</a>
                    </p>
                    <p class="box_tour ret">
                        <img class="icon fone" src="@/assets/telefone.svg" alt="icone telefone">
                        <a href="#">Tour Virtual</a>
                    </p>
                    <p class="box_wpp ret">
                        <img class="icon fone" src="@/assets/Icon_whatsapp.svg" alt="icone whatsapp">
                        <a href="#">whatsapp</a>
                    </p>
                </div>
                <img class="logo logo_desk" src="@/assets/logo-bmw-rio.svg" alt="logo bmw">
            </div>
            <div class="bottom">
                <dropComponent></dropComponent>
            </div>
        </div>
    </div>
</template>
<script>
import dropComponent from './drop.vue';
export default {
    name: 'headerComponent',
    components: { dropComponent },
}
</script>

<style scoped>
.container {
    display: flex;
    justify-content: space-between;
    align-items: center;
    margin: auto 5%;
}
.header_mobile{
    display: flex;
    width: 100vw;
    justify-content: space-around;
    align-items: center;
}
.header_desktop {
    display: none;
}

.logo {
    width: 34px;
    height: 34px;
}

a {
    color: #666666;
    text-decoration: none;
}

.box_tel {
    display: flex;
}

.fone {
    width: 19px;
    margin-right: 8px;
}

@media(min-width: 765px) {
    .header_mobile {
        display: none;
    }

    .header_desktop {
        margin-top: 20px;
        display: block;
    }

    .rets {
        display: flex;
    }

    .ret {
        width: 110px;
        padding: 10px;
        background-color: #000000;
        margin-right: 8px;
        font-size: 12px;
        text-align: center;
        display: flex;
        justify-content: center;
        align-items: center;
    }

    .box_wpp {
        background-color: #25D366;
    }

    .icon {
        filter: invert(99%) sepia(7%) saturate(127%) hue-rotate(223deg) brightness(116%) contrast(100%);
    }

    .icon:hover {
        cursor: pointer;
        filter: invert(27%) sepia(97%) saturate(1378%) hue-rotate(198deg) brightness(100%) contrast(90%);
    }

    a {
        color: #FFFFFF;
    }

    .top {
        display: flex;
        min-width: 90vw;
        justify-content: space-around;
        align-items: center;
    }

    .logo_desk {
        width: 75px;
        height: 75px;
    }
}
</style>