<template>
    <section class="main">
        <section class="toggles">
            <svg width="22" height="22" viewBox="0 0 22 22" fill="none" xmlns="http://www.w3.org/2000/svg"
                @click="clickToggle" style="cursor: pointer;">
                <rect width="6" height="6" :fill="`${currentColor}`" />
                <rect x="8" width="6" height="6" :fill="`${currentColor}`" />
                <rect x="16" width="6" height="6" :fill="`${currentColor}`" />
                <rect y="8" width="6" height="6" :fill="`${currentColor}`" />
                <rect y="16" width="6" height="6" :fill="`${currentColor}`" />
                <rect x="8" y="8" width="6" height="6" :fill="`${currentColor}`" />
                <rect x="8" y="16" width="6" height="6" :fill="`${currentColor}`" />
                <rect x="16" y="8" width="6" height="6" :fill="`${currentColor}`" />
                <rect x="16" y="16" width="6" height="6" :fill="`${currentColor}`" />
            </svg>

            <svg width="24" height="22" viewBox="0 0 24 22" fill="none" xmlns="http://www.w3.org/2000/svg"
                @click="clickToggle" style="cursor: pointer;">
                <rect width="6" height="6" :fill="`${curentReverseColor}`" />
                <rect y="8" width="6" height="6" :fill="`${curentReverseColor}`" />
                <rect y="16" width="6" height="6" :fill="`${curentReverseColor}`" />
                <rect x="9" y="10" width="15" height="2" :fill="`${curentReverseColor}`" />
                <rect x="9" y="18" width="15" height="2" :fill="`${curentReverseColor}`" />
                <rect x="9" y="2" width="15" height="2" :fill="`${curentReverseColor}`" />
            </svg>
        </section>

        <section>
            <div :class="`${cardListDirection}`">
                <div class="column card" v-for="(card, index) in cards" :key="index">
                    <ProductCardRow v-if="`${cardListDirection}` === 'column'" :imageName="card.imageName" />
                    <ProductCardColumn v-if="`${cardListDirection}` === 'row'" :imageName="card.imageName" />
                </div>
            </div>
        </section>

        <button class="load-more">LOAD MORE</button>
    </section>
</template>

<script setup>
import ProductCardRow from './ProductCardRow.vue'
import ProductCardColumn from './ProductCardColumn.vue'
import { ref, computed } from 'vue';

const currentIndex = ref(0);
const curentReverseIndex = ref(1);

const toggle = ref([
    { color: '#3D8EDA', direction: 'row' },
    { color: '#C8C7C7', direction: 'column' }
]);

const currentColor = computed(() => toggle.value[currentIndex.value].color);
const curentReverseColor = computed(() => toggle.value[curentReverseIndex.value].color);
const cardListDirection = computed(() => toggle.value[currentIndex.value].direction);

function clickToggle() {
    currentIndex.value = (currentIndex.value + 1) % toggle.value.length;
    curentReverseIndex.value = (curentReverseIndex.value + 1) % toggle.value.length;
}

const cards = ref([])

const imagesContext = require.context('@/assets/images', false, /\.jpg$/)
cards.value = imagesContext.keys().map((imageFileName) => {
    return {
        imageName: imagesContext(imageFileName),
    }
})
</script>


<style scoped>
.main {
    display: flex;
    flex-direction: column;
    max-width: 836px;
    margin: auto;
    margin-top: 190px;
}

@media (max-width: 1024px) {
    .main {
        margin-top: 350px;
    }
}

@media (max-width: 768px) {
    .main {
        margin-top: 350px;
    }
}

.toggles {
    width: 100%;
    text-align: right;
    margin-bottom: 20px;
}

svg {
    margin-left: 22px;
}

.row {
    display: flex;
    flex-direction: row;
    gap: 7px;
    width: 100%;
    flex-wrap: wrap;
}

.column {
    flex-direction: column;
    flex: 23%;
}

.load-more {
    border-radius: 14px;
    border: 1px solid rgba(146, 146, 146, 1);
    color: #929292;
    letter-spacing: -0.33px;
    display: flex;
    justify-content: center;
    max-width: 111px;
    padding: 5px 10px;
    margin: 20px auto;
    font: 500 11px Roboto, sans-serif;
    cursor: pointer;
}
</style>