<template>
    <div class="container">
        <div class="numbers">
            <p v-for="number in numbers" :key="number" @click="select">{{ number }}</p>
        </div>
        <div class="divider">
            <hr v-if="selected">
        </div>
        <div class="cards" v-if="selected">
            <cardComponent class="card" :carro="require('@/assets/serie1.png')" title="BMW Série 1"></cardComponent>
            <cardComponent class="card" :carro="require('@/assets/serie1.png')" title="BMW Série 1"></cardComponent>
            <cardComponent class="card" :carro="require('@/assets/serie1.png')" title="BMW Série 1"></cardComponent>
            <cardComponent class="card" :carro="require('@/assets/serie1.png')" title="BMW Série 1"></cardComponent>
        </div>
    </div>
</template>

<script>
import cardComponent from './card.vue'
export default {
    name: 'dropComponent',
    components: {
        cardComponent
    },
    data() {
        return {
            numbers: ['1', '2', '3', '4', '5', '6', '7', '8', 'X', 'Z', 'M', 'I', 'Plug-in-Hybrid'],
            selected: false
        }
    },
    methods: {
        select() {
            this.selected = !this.selected;
        },
    },
}
</script>
<style scoped>

.container{
    flex-direction: column;
}
.cards {
    display: flex;
    gap: 20px;
}

.card {
    width: auto;
}

.numbers {
    display: flex;
    justify-content: center;
    align-items: center;
    gap: 20px;
}

.numbers p {
    cursor: pointer;
    padding-right: 20px;
}
.divider{
    width: 80vw;
}
</style>