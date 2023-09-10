<template>
    <div class="the-wrapper">
        <TheToolbar>

        </TheToolbar>
        <slot>
            
        </slot>
    </div>
</template>

<script>
import TheToolbar from './TheToolbar.vue';

export default {
    name: 'App',
    components: {
        TheToolbar
    }
}
</script>

<style scoped>
    .the-wrapper {
        margin: 0 50px 0 50px;
    }
</style>