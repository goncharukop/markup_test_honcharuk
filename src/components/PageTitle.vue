<template>
  <section>
    <svg width="630" height="398" viewBox="0 0 630 398" fill="none" xmlns="http://www.w3.org/2000/svg"
      class="responsive-image">
      <path
        d="M143 351C85.8 414.2 23.8333 399.667 0 384.5L-59 308L-54 1.5L287.5 -84.5L630 -3.5C582.4 11.7 571 23 564.5 52C553.49 101.12 525.333 156 511.5 169.5C457.5 243 363.5 215.5 307 214.5C250.5 213.5 212.5 229.5 191.5 271C175.499 302.622 154 338.167 143 351Z"
        fill="url(#paint0_linear_1_3)" />
      <defs>
        <linearGradient id="paint0_linear_1_3" x1="536.5" y1="-84" x2="54.5" y2="398" gradientUnits="userSpaceOnUse">
          <stop stop-color="#40AF79" />
          <stop offset="1" stop-color="#124757" />
        </linearGradient>
      </defs>
    </svg>
  </section>
  <section class="shadowed-container"></section>
  <section class="logo-container">
    <svg width="138" height="138" viewBox="0 0 138 138" fill="none" xmlns="http://www.w3.org/2000/svg" class="logo-img">
      <path
        d="M56.5 7.21688C64.235 2.75106 73.765 2.75106 81.5 7.21688L116.256 27.2831C123.991 31.7489 128.756 40.0021 128.756 48.9338V89.0662C128.756 97.9979 123.991 106.251 116.256 110.717L81.5 130.783C73.765 135.249 64.235 135.249 56.5 130.783L21.7442 110.717C14.0092 106.251 9.24425 97.9979 9.24425 89.0662V48.9338C9.24425 40.0021 14.0092 31.7489 21.7442 27.2831L56.5 7.21688Z"
        fill="white" />
      <path
        d="M128.756 88.5317V89.0662C128.756 97.9979 123.991 106.251 116.256 110.717L81.5 130.783C73.765 135.249 64.235 135.249 56.5 130.783L21.7442 110.717C21.1716 110.386 20.6152 110.035 20.0758 109.664L17.5 101L26 68L33.5 56L55.5 78.5L82.5 38.5L128.756 88.5317Z"
        fill="#066C61" />
      <path
        d="M18.1726 108.216C14.6282 105.242 11.9954 101.354 10.5392 97.0093L10.5 96.5C11.6667 83.5 16.7 56.8 27.5 54C41.5 50.3704 48.5 96.5 48.5 96.5C48.5 96.5 54.7204 32.2562 74 33.5C89.5 34.5 95.5 66.5 91.5 125L91.4793 125.022L81.5 130.783C78.1083 132.741 74.3715 133.841 70.5923 134.082C77.5658 121.943 76.9064 74.0186 73.5 56.5C71.5082 62.0157 69.939 70.5009 68.2456 79.6575C64.4128 100.382 59.9439 124.546 48.5 125.5C48.0761 125.535 47.6559 125.513 47.2396 125.437L43.4536 123.251C36.248 116.272 30.6804 94.8558 28.5 83C28.103 93.7195 24.061 105.982 22.0451 110.891L21.7442 110.717C21.4834 110.566 21.2259 110.411 20.9718 110.252L18.1726 108.216Z"
        fill="#B3DBC9" />
    </svg>
  </section>

  <section class="project-details">
    <header class="project-header">
      <h1 class="project-title">monblanproject</h1>
      <time class="start-date" datetime="2016-02-17">Start on 17-02-2016</time>
    </header>
    <section class="project-stats">
      <div class="stat-item">
        <span class="stat-number">870 </span>
        <span class="stat-label">posts</span>
      </div>
      <div class="stat-item">
        <span class="stat-number">11,787 </span>
        <span class="stat-label">followers</span>
      </div>
      <div class="stat-item">
        <span class="stat-number">112 </span>
        <span class="stat-label">following</span>
      </div>
    </section>

    <div class="date">
      <label class="date-text" for="datepicker">Date</label>
      <flat-pickr v-model="dateFrom" :config="config"></flat-pickr>
      <flat-pickr v-model="dateTo" :config="config"></flat-pickr>
    </div>
  </section>
</template>

<script setup>
import { ref } from 'vue';
import flatPickr from 'vue-flatpickr-component';
import 'flatpickr/dist/flatpickr.css';

const dateFrom = ref(null);
const dateTo = ref(null);

const config = {
  enableTime: false,
  dateFormat: 'd-m-Y',
  locale: {
    firstDayOfWeek: 1
  },
  defaultDate: '09-08-2016',
};
</script>

<style scoped>
.responsive-image {
  position: absolute;
  top: 0;
  left: 0;
  width: 100%;
  max-width: 630px;
}

.shadowed-container {
  position: absolute;
  top: 0;
  left: 0;
  box-shadow: inset 0 12px 24px rgba(0, 0, 0, 0.12), 0 4px 24px rgba(0, 0, 0, 0.12);
  background-color: rgba(255, 255, 255, 0.67);
  width: 100%;
  min-height: 172px;
}

.logo-container {
  position: absolute;
  top: 6px;
  left: 355px;
  width: 138px;
}

.logo-img {
  object-fit: cover;
  width: 100%;
  max-width: 120px;
}

.project-details {
  display: flex;
  flex-direction: column;
  position: absolute;
  top: 33px;
  left: 579px;
  max-width: 346px;
}

.project-header {
  display: flex;
  gap: 20px;
}

.project-title {
  color: #000;
  letter-spacing: -0.24px;
  margin: auto 0;
  font: 500 24px Montserrat, sans-serif;
  flex-grow: 1;
}

.start-date {
  border: 1px solid rgba(61, 142, 218, 1);
  color: #3d8eda;
  letter-spacing: -0.39px;
  padding: 5px 12px;
  font: 400 13px Roboto, sans-serif;
  border-radius: 2px;
  text-align: center;
}

.project-stats {
  display: flex;
  gap: 19px;
  margin-top: 17px;
  font-size: 14px;
  color: #000;
  font-weight: 500;
}

.stat-item {
  font-family: Roboto, sans-serif;
}

.stat-number {
  font-weight: 700;
}

.stat-label {
  font-weight: 400;
}

.date {
  display: flex;
  gap: 20px;
  margin-top: 20px;
}

.date-text {
  color: #000;
  max-width: 31px;
  font: 400 16px Roboto, sans-serif;
}

@media (max-width: 1024px) {
  .logo-container {
    top: 6px;
    left: 50%;
    transform: translateX(-60%);
  }

  .project-details {
    top: 200px;
    left: 50%;
    transform: translateX(-50%);
  }
}

@media (max-width: 768px) {
  .responsive-image {
    max-width: 80%;
    transform: translateY(-70px);
  }

  .logo-container {
    width: 100px;
  }

  .project-details {
    min-width: 300px;
    padding: 0 20px;
  }

  .project-title {
    font-size: 20px;
  }

  .start-date {
    font-size: 11px;
    padding: 3px 8px;
  }

  .project-stats {
    gap: 10px;
  }

  .date {
    flex-direction: column;
    gap: 10px;
  }

  .date-text {
    font-size: 14px;
  }
}

@media (max-width: 480px) {
  .responsive-image {
    min-width: 480px;
  }

  .shadowed-container {
    min-height: 120px;
  }

  .logo-container {
    top: 0;
    width: 80px;
  }

  .project-details {
    top: 160px;
    padding: 0 10px;
  }

  .project-title {
    font-size: 18px;
  }

  .start-date {
    font-size: 10px;
    padding: 2px 6px;
  }

  .project-stats {
    gap: 5px;
  }

  .date {
    gap: 5px;
  }

  .date-text {
    font-size: 12px;
  }
}
</style>
