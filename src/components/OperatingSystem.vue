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
  <section class="p-10">
    <div class="max-w-[1140px] mx-auto">
      <div class="grid grid-cols-2 gap-8">
        <div>
          <img :src="LeftImage" alt="" />
        </div>
        <div class="pt-10 px-10">
          <h3 class="text-[44px] font-bold leading-[130%]">It’s helpful for operating system</h3>
          <div
            v-for="(operatinSystem, index) in operatingSystems"
            :key="index"
            class="mb-[30px]"
            :class="{ 'mb-[30px]': index > 0, 'mt-[30px]': index === 0 }"
          >
            <div class="flex items-center">
              <ArrowIcon :color="operatinSystem.iconColor" />
              <h5 class="text-[25px] font-medium leading-[150%] ml-3">
                {{ operatinSystem.title }}
              </h5>
            </div>
            <p class="text-[14px] font-normal leading-[160%] ml-9">
              {{ operatinSystem.description }}
            </p>
          </div>
        </div>
      </div>
    </div>
  </section>
</template>
