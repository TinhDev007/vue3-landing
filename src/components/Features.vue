<script setup lang="ts">
import { ref } from 'vue'
import IconCircleArrow from './icons/IconCircleArrow.vue'
import IconCleanCode from '../assets/cleanCodeIcon.svg'
import IconDataAnalytics from '../assets/dataAnalytics.svg'
import IconFullySecured from '../assets/fullySecured.svg'
import IconFullSupport from '../assets/fullSupport.svg'

const featureList = ref([
  {
    id: 1,
    icon: IconCleanCode,
    title: 'Clean Code',
    description: 'Lorem ipsum dolor sit amet ecte adipiscing elitIpsum.'
  },
  {
    id: 2,
    icon: IconDataAnalytics,
    title: 'Data Analytic',
    description: 'Lorem ipsum dolor sit amet ecte adipiscing elitIpsum.'
  },
  {
    id: 3,
    icon: IconFullySecured,
    title: 'Fully Secured',
    description: 'Lorem ipsum dolor sit amet ecte adipiscing elitIpsum.'
  },
  {
    id: 4,
    icon: IconFullSupport,
    title: '24/7 Support',
    description: 'Lorem ipsum dolor sit amet ecte adipiscing elitIpsum.'
  }
])
</script>

<template>
  <section>
    <div class="container mx-auto">
      <h3 class="text-center max-w-[549px] mx-auto mb-[60px] text-[44px] font-bold leading-[130%]">
        We Provides best Feature for customers
      </h3>
      <div class="grid grid-cols-4 gap-4">
        <div
          class="flex flex-col items-center text-center max-w-[263px] mx-auto shadow-[0_6px_50px_5px_rgba(6,14,26,0.05)] p-10"
          v-for="(featureItem, index) in featureList"
          :key="index"
        >
          <div class="mb-[50px]">
            <img :src="featureItem.icon" alt="" />
          </div>
          <div>
            <h5>{{ featureItem.title }}</h5>
            <p>
              {{ featureItem.description }}
            </p>
          </div>
          <IconCircleArrow />
        </div>
      </div>
    </div>
  </section>
</template>
