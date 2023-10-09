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
  <div>
    <h3>We Provides best Feature for customar</h3>
    <div>
      <div v-for="(featureItem, index) in featureList" :key="index">
        <div>
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
</template>
