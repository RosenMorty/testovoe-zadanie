<template>
    <div class="cardbar-user">
        <img 
        :src="props.image"
        alt="ItemCard"
        class="cardbar-image"
        >
        <h1 class="cardbar-title">{{ props.title }}</h1>
        <div class="cardbar-mail">{{ props.mail }}</div>
    </div>
</template>

<script setup>
import { defineProps } from 'vue';

const props = defineProps(['image', 'title', 'mail'])

</script>