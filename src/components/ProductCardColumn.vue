<template>
    <div class="main-container">
        <div class="responsive-flex">
            <section class="content-column">
                <div class="content-card">
                    <img loading="lazy" :src="imageName" alt="card photo" class="card-image" />

                    <div class="row">
                        <div class="column date">Today</div>
                        <div class="column date">9-08-2016</div>
                    </div>
                    <div class="row">
                        <div class="column icon-count">
                            <svg width="16" height="14" viewBox="0 0 16 14" fill="none" xmlns="http://www.w3.org/2000/svg">
                                <path
                                    d="M0.5 4.3C0.499908 3.76178 0.607097 3.22893 0.815302 2.73261C1.02351 2.23629 1.32855 1.78645 1.71261 1.40937C2.09667 1.0323 2.55203 0.735557 3.05209 0.536492C3.55215 0.337428 4.08687 0.240033 4.625 0.25C5.26172 0.246619 5.89189 0.378602 6.47374 0.637203C7.05559 0.895804 7.57584 1.27512 8 1.75C8.42416 1.27512 8.9444 0.895804 9.52626 0.637203C10.1081 0.378602 10.7383 0.246619 11.375 0.25C11.9131 0.240033 12.4479 0.337428 12.9479 0.536492C13.448 0.735557 13.9033 1.0323 14.2874 1.40937C14.6714 1.78645 14.9765 2.23629 15.1847 2.73261C15.3929 3.22893 15.5001 3.76178 15.5 4.3C15.5 8.317 10.7157 11.35 8 13.75C5.29025 11.3298 0.5 8.32 0.5 4.3Z"
                                    fill="black" />
                            </svg>
                            <div class="count-text">128</div>
                        </div>
                        <div class="column icon-count">
                            <svg width="16" height="14" viewBox="0 0 16 14" fill="none" xmlns="http://www.w3.org/2000/svg">
                                <path
                                    d="M0.5 4.3C0.499908 3.76178 0.607097 3.22893 0.815302 2.73261C1.02351 2.23629 1.32855 1.78645 1.71261 1.40937C2.09667 1.0323 2.55203 0.735557 3.05209 0.536492C3.55215 0.337428 4.08687 0.240033 4.625 0.25C5.26172 0.246619 5.89189 0.378602 6.47374 0.637203C7.05559 0.895804 7.57584 1.27512 8 1.75C8.42416 1.27512 8.9444 0.895804 9.52626 0.637203C10.1081 0.378602 10.7383 0.246619 11.375 0.25C11.9131 0.240033 12.4479 0.337428 12.9479 0.536492C13.448 0.735557 13.9033 1.0323 14.2874 1.40937C14.6714 1.78645 14.9765 2.23629 15.1847 2.73261C15.3929 3.22893 15.5001 3.76178 15.5 4.3C15.5 8.317 10.7157 11.35 8 13.75C5.29025 11.3298 0.5 8.32 0.5 4.3Z"
                                    fill="black" />
                            </svg>
                            <div class="count-text">67</div>
                        </div>
                    </div>
                    <div class="row">
                        <div class="column icon-count">
                            <svg width="16" height="16" viewBox="0 0 16 16" fill="none" xmlns="http://www.w3.org/2000/svg">
                                <path
                                    d="M15.5 2C15.5 1.175 14.825 0.5 14 0.5H2C1.175 0.5 0.5 1.175 0.5 2V11C0.5 11.825 1.175 12.5 2 12.5H12.5L15.5 15.5V2Z"
                                    fill="black" />
                            </svg>
                            <div class="additional-count-text">31</div>
                        </div>
                        <div class="column icon-count">
                            <svg width="16" height="16" viewBox="0 0 16 16" fill="none" xmlns="http://www.w3.org/2000/svg">
                                <path
                                    d="M15.5 2C15.5 1.175 14.825 0.5 14 0.5H2C1.175 0.5 0.5 1.175 0.5 2V11C0.5 11.825 1.175 12.5 2 12.5H12.5L15.5 15.5V2Z"
                                    fill="black" />
                            </svg>
                            <div class="additional-count-text">22</div>
                        </div>
                    </div>

                    <div class="row row-upload">
                        <div class="column column-main upload-label">Image upload</div>
                        <div class="column upload-date">11-04-2016</div>
                    </div>
                </div>
            </section>
        </div>
    </div>
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
    max-width: 200px;
    margin-top: 0px;
}

.responsive-flex {
    gap: 20px;
    display: flex;

}

@media (max-width: 991px) {
    .responsive-flex {
        flex-direction: column;
        align-items: stretch;
        gap: 0;
    }
}

.content-column {
    display: flex;
    flex-direction: column;
    line-height: normal;
    width: 203px;
    margin-left: 0;

}

@media (max-width: 991px) {
    .content-column {
        width: 100%;
    }
}

.content-card {
    display: flex;
    width: 100%;
    flex-grow: 1;
    padding-bottom: 18px;
    flex-direction: column;
    color: #000;
    background-color: #fff;
    font-weight: 500;
    margin: 0 auto;
}

.card-image {
    aspect-ratio: 1;
    object-fit: auto;
    object-position: center;
    width: 203px;
    height: 203px;
    align-self: center;
    padding-bottom: 15px;
}

.row {
    display: flex;
    gap: 20px;
}

.row-upload {
    gap: 15px;
    justify-content: space-between;
    padding-top: 20px;
}

.column {
    flex: 50%;
    padding-left: 10px;
    text-align: left;
}

.column-main {
    flex: 70%;
}

.date {
    font: 16px Roboto, sans-serif;
}

.icon-count {
    display: flex;
    margin-top: 8px;
    gap: 6px;
    font-size: 14px;
}


.count-text,
.additional-count-text {
    font-family: Roboto, sans-serif;
    margin: auto 0;
}

.upload-label {
    font: 14px Roboto, sans-serif;
}

.upload-date {
    font: 12px Roboto, sans-serif;
}</style>