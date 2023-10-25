<template>
    <div class="container">
        <button v-if="!showForm" class="maxi" @click="toggleForm">
            Solicite uma cotação
        </button>
        <div class="over" v-if="showForm">
            <div class="modal">
                <button class="mini" @click="toggleForm">
                    Minimizar
                </button>
                <div class="calculadora">
                    <img class="calc_img" src="@/assets/Icon_calculadora.svg" alt="icone carro">
                    <p style="font-size: 20px; color: #000000;">Solicitar Cotação</p>
                </div>

                <form v-if="showForm" @submit.prevent="submitForm" class="form_fields">
                    <input type="text" id="nome" v-model="formData.nome" placeholder="Nome">
                    <input type="email" id="email" v-model="formData.email" placeholder="E-mail">
                    <input type="tel" id="telefone" v-model="formData.telefone" placeholder="Telefone">
                    <select id="model" v-model="formData.model" class="model">
                        <option value="modelo">Modelo</option>
                        <option value="bmw">BMW</option>
                        <option value="bmw2">BMW2</option>
                        <option value="bmw3">BMW3</option>
                    </select>
                    <input type="text" id="message" v-model="formData.message" placeholder="Mensagem">
                    <div class="checkB">
                        <input name="termos" id="termos" type="checkbox" v-model="formData.aceitaTermos">
                        <label for="termos" style="font-size: 12px; color:#666666 ;"> Aceito a <span
                                style="font-weight: bold;">Política e privacidade</span>
                        </label>
                    </div>
                    <button class="enviar" type="submit">Enviar</button>
                </form>
            </div>
        </div>
    </div>
</template>
<script>
export default {
    name: 'formCotacao',
    data() {
        return {
            showForm: true,
            formData: {
                nome: '',
                email: '',
                telefone: '',
                message: '',
                model: 'modelo',
                aceitaTermos: false
            }
        };
    },
    methods: {
        toggleForm() {
            this.showForm = !this.showForm;
        },
        submitForm() {
            this.showForm = false;
        }
    }
}
</script>
<style scoped>
.modal {
    position: fixed;
    top: 0;
    width: 100%;
    height: fit-content;
    z-index: 999;
    background-color: #fff;
    padding-bottom: 20px;
}

.maxi,
.mini,
.enviar {
    color: #FFFFFF;
    width: 100%;
    padding-top: 15px;
    padding-bottom: 15px;
    border-style: none;
    font-weight: bold;

}

.maxi,
.enviar {
    background-color: #1C69D4;
}

.enviar {
    width: 90%;
}

.enviar:hover {
    cursor: pointer;
    background-color: #0351BE;
}

.mini {
    background-color: #666666;

}

.mini:hover {
    cursor: pointer;
}

.maxi:hover {
    cursor: pointer;
    background-color: #0351BE;
}

.form_fields {
    display: flex;
    flex-direction: column;
    justify-content: center;
    align-items: center;
}

input {
    padding-top: 10px;
    padding-bottom: 10px;
    border: none;
    border-bottom: 1px solid #BBBBBB;
    outline: none;
    width: 90%;
}

input:hover {
    cursor: pointer;
    border-bottom: 2px solid #8f8d8d;
}

input:focus {
    border-color: #1C69D4;
}

.model {
    border: none;
    background-color: #fff;
    color: #666666;
    border-bottom: 1px solid #8f8d8d;
    padding-top: 10px;
    padding-bottom: 10px;
    width: 90%;
}

.model:focus {
    border-color: #1C69D4;
    outline: none;
}

.calculadora {
    display: flex;
    justify-content: center;
    align-items: center;
    margin-top: 20px;
}

.calc_img {
    margin-right: 10px;
}

.checkB {
    margin-top: 20px;
    margin-bottom: 20px;
    display: flex;
    align-items: center;
    justify-content: start;
    width: 90%;
}

.checkB input[type="checkbox"] {
    width: min-content;
    margin-right: 5px;
}

@media(min-width: 765px) {

    .mini,
    .maxi {
        display: none;
    }
    .modal {
        position: fixed;
        width: 300px;
        top: 50%;
        right: 10%;
    }
}
</style>