<script setup lang="ts">
import { ref, h } from 'vue'

import SwiperTest from '../components/SwiperTest.vue'

const swiper = ref(true)

const vnode = h('div', ['test'])
</script>

<template>
    <main>
        <component
            :is="swiper ? SwiperTest : vnode"
            @vue:before-mount="swiper = false"
            @vue:mounted="console.log('mounted', $event)"
            @vue:unmounted="console.log('unmounted', $event)"
        ></component>
    </main>
</template>
