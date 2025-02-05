<template>
    <Swiper
        :loop="true"
        @swiper="console.log('onSwiper', $event)"
    >
        <SwiperSlide>Slide 1</SwiperSlide>
        <SwiperSlide>Slide 2</SwiperSlide>
        <SwiperSlide>Slide 3</SwiperSlide>
        ...
    </Swiper>
</template>
<script lang="ts" setup>
import { onMounted, onUnmounted } from 'vue'
import { Swiper, SwiperSlide } from 'swiper/vue'

import 'swiper/css'

onMounted(() => {
    console.log('onMounted')
})

onUnmounted(() => {
    console.log('onUnmounted')
})
</script>
