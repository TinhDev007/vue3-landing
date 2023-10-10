<script setup lang="ts">
import { ref } from 'vue'
import ArrowIcon from './icons/IconArrow.vue'
import LeftImage from '../assets/operatingLeftImage.svg'

const operatingSystems = ref([
  {
    id: 1,
    iconColor: '#ef821e',
    title: 'Ultra fast & Secure',
    description:
      'Lorem ipsum dolor sit amet, consectetur adipiscing elit. vitae velit proin justo elementum siIn morbi'
  },
  {
    id: 2,
    iconColor: '#5ebd14',
    title: 'Allows customization',
    description:
      'Lorem ipsum dolor sit amet, consectetur adipiscing elit. vitae velit proin justo elementum siIn morbi'
  },
  {
    id: 3,
    iconColor: '#3b87fa',
    title: 'Smart contract',
    description:
      'Lorem ipsum dolor sit amet, consectetur adipiscing elit. vitae velit proin justo elementum siIn morbi'
  }
])
</script>

<template>
  <section class="operating-system-section">
    <div class="container mx-auto grid grid-cols-2 gap-4">
      <div>
        <img :src="LeftImage" alt="" />
      </div>
      <div>
        <h3>It’s helpful for operating system</h3>
        <div v-for="(operatinSystem, index) in operatingSystems" :key="index">
          <div>
            <ArrowIcon :color="operatinSystem.iconColor" />
            <h5>{{ operatinSystem.title }}</h5>
          </div>
          <p>
            {{ operatinSystem.description }}
          </p>
        </div>
      </div>
    </div>
  </section>
</template>
