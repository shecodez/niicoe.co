<template>
  <h1>{{ msg }}</h1>
  <p>Site under construction.</p>
  <div>~🥰 Niico</div>
  <p>
    <a href="https://www.instagram.com/niicoe_co/">Instagram</a> · <a href="https://twitter.com/niicoe_co">Twitter</a> ·
    <a href="https://www.youtube.com/channel/UCpbqKabuyhsqgwr4m6042zA"> YouTube </a> ·
    <a href="https://www.tiktok.com/@niicoe_co">TikTok</a>
  </p>
</template>

<script setup>
import { defineProps, reactive } from 'vue';

defineProps({
  msg: String,
});

const state = reactive({ count: 0 });
</script>
