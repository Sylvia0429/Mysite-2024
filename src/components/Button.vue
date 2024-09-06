<template>
  <a :class="`btn bg-[${bgColor}] text-${textColor} px-6 hover:bg-[${hoverBgColor}]`">{{ text }}</a>
</template>

<script setup>
import { defineProps } from 'vue'

const props = defineProps({
  text: String,
  bgColor: String,
  textColor: String,
  hoverBgColor: String,
})
</script>