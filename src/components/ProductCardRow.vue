<template>
    <section class="main-container">
        <div class="content-wrapper">
            <div class="image-container">
                <img loading="lazy" :src="imageName" alt="card photo" />
                <div class="info-container">
                    <time datetime="2023-10-04" class="date">Today</time>
                    <div class="stats">
                        <div class="stat-item">
                            <svg width="16" height="14" viewBox="0 0 16 14" fill="none" xmlns="http://www.w3.org/2000/svg">
                                <path
                                    d="M0.5 4.3C0.499908 3.76178 0.607097 3.22893 0.815302 2.73261C1.02351 2.23629 1.32855 1.78645 1.71261 1.40937C2.09667 1.0323 2.55203 0.735557 3.05209 0.536492C3.55215 0.337428 4.08687 0.240033 4.625 0.25C5.26172 0.246619 5.89189 0.378602 6.47374 0.637203C7.05559 0.895804 7.57584 1.27512 8 1.75C8.42416 1.27512 8.9444 0.895804 9.52626 0.637203C10.1081 0.378602 10.7383 0.246619 11.375 0.25C11.9131 0.240033 12.4479 0.337428 12.9479 0.536492C13.448 0.735557 13.9033 1.0323 14.2874 1.40937C14.6714 1.78645 14.9765 2.23629 15.1847 2.73261C15.3929 3.22893 15.5001 3.76178 15.5 4.3C15.5 8.317 10.7157 11.35 8 13.75C5.29025 11.3298 0.5 8.32 0.5 4.3Z"
                                    fill="black" />
                            </svg>
                            <div class="count-text">128</div>
                        </div>
                        <div class="stat-item">
                            <svg width="16" height="16" viewBox="0 0 16 16" fill="none" xmlns="http://www.w3.org/2000/svg">
                                <path
                                    d="M15.5 2C15.5 1.175 14.825 0.5 14 0.5H2C1.175 0.5 0.5 1.175 0.5 2V11C0.5 11.825 1.175 12.5 2 12.5H12.5L15.5 15.5V2Z"
                                    fill="black" />
                            </svg>
                            <span class="stat-value">31</span>
                        </div>
                    </div>
                </div>
                <div class="info-container detail">
                    <time datetime="2016-08-09" class="date">9-08-2016</time>
                    <div class="stats">
                        <div class="stat-item">
                            <svg width="16" height="14" viewBox="0 0 16 14" fill="none" xmlns="http://www.w3.org/2000/svg">
                                <path
                                    d="M0.5 4.3C0.499908 3.76178 0.607097 3.22893 0.815302 2.73261C1.02351 2.23629 1.32855 1.78645 1.71261 1.40937C2.09667 1.0323 2.55203 0.735557 3.05209 0.536492C3.55215 0.337428 4.08687 0.240033 4.625 0.25C5.26172 0.246619 5.89189 0.378602 6.47374 0.637203C7.05559 0.895804 7.57584 1.27512 8 1.75C8.42416 1.27512 8.9444 0.895804 9.52626 0.637203C10.1081 0.378602 10.7383 0.246619 11.375 0.25C11.9131 0.240033 12.4479 0.337428 12.9479 0.536492C13.448 0.735557 13.9033 1.0323 14.2874 1.40937C14.6714 1.78645 14.9765 2.23629 15.1847 2.73261C15.3929 3.22893 15.5001 3.76178 15.5 4.3C15.5 8.317 10.7157 11.35 8 13.75C5.29025 11.3298 0.5 8.32 0.5 4.3Z"
                                    fill="black" />
                            </svg>
                            <span class="stat-value">67</span>
                        </div>
                        <div class="stat-item">
                            <svg width="16" height="16" viewBox="0 0 16 16" fill="none" xmlns="http://www.w3.org/2000/svg">
                                <path
                                    d="M15.5 2C15.5 1.175 14.825 0.5 14 0.5H2C1.175 0.5 0.5 1.175 0.5 2V11C0.5 11.825 1.175 12.5 2 12.5H12.5L15.5 15.5V2Z"
                                    fill="black" />
                            </svg>
                            <span class="stat-value">22</span>
                        </div>
                    </div>
                </div>
                <div class="info-container detail">
                    <label for="imageUpload" class="label">Image upload</label>
                    <time datetime="2016-04-11" class="date">11-04-2016</time>
                </div>
            </div>
        </div>
    </section>
</template>

<script setup>
import { defineProps } from 'vue'

// eslint-disable-next-line
const props = defineProps({
    imageName: String
})

</script>

<style scoped>
.main-container {
    display: flex;
    flex-direction: column;
    max-width: 836px;
    color: #000;
    font-weight: 500;
}

.content-wrapper {
    background-color: #fff;
    display: flex;
    flex-direction: column;
    width: 100%;
    padding-right: 80px;
    gap: 20px;
    justify-content: space-between;
    margin-top: 8px;
}

@media (max-width: 991px) {
    .content-wrapper {
        flex-wrap: wrap;
        padding-right: 20px;
    }
}

.image-container {
    display: flex;
    gap: 20px;
    justify-content: space-between;
}

.image-container img {
    width: 86px;
}

.info-container {
    display: flex;
    flex-direction: column;
    justify-content: center;
}

.date {
    font-family: Roboto, sans-serif;
    font-size: 16px;
    text-align: left;
}

.stats {
    display: flex;
    gap: 20px;
    font-size: 14px;
    margin-top: 8px;
}

.stat-item {
    display: flex;
    align-items: center;
    gap: 6px;
}

.stat-item img {
    width: 18px;
}

.stat-value {
    font-family: Roboto, sans-serif;
}

.detail {
    display: flex;
    flex-direction: column;
    align-items: flex-start;
}

.label {
    font-family: Roboto, sans-serif;
    font-size: 16px;
    margin-bottom: 10px;
}

@media (max-width: 991px) {
    .detail {
        flex: 1;
    }
}
</style>