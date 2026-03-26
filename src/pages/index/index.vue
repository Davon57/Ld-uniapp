<template>
  <web-view :src="targetUrl" />
</template>

<script setup lang="ts">
import { ref } from 'vue'
import { onLoad } from '@dcloudio/uni-app'

const DEFAULT_URL = 'http://davon-ld.icu/'
const targetUrl = ref(DEFAULT_URL)

onLoad(() => {
  let title = '蓝友圈'
  const match = targetUrl.value.match(/^https?:\/\/([^/]+)/i)
  if (match?.[1]) title = match[1]
  uni.setNavigationBarTitle({ title })
})
</script>

<style></style>
