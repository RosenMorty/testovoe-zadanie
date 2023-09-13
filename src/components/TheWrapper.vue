<template>
    <div class="the-wrapper">

        <TheToolbar></TheToolbar>
        <TheSearchbar></TheSearchbar>
        <TheResult></TheResult>
        <slot>
            
        </slot>
    </div>
</template>

<script>
import TheToolbar from './TheToolbar.vue';
import TheSearchbar from './TheSearchbar.vue';
import TheResult from './TheResult.vue'



export default {
    name: 'App',
    components: {
        TheToolbar,
        TheSearchbar,
        TheResult
    }
}
</script>

<style scoped>
    .the-wrapper {
        margin: 0 50px 0 50px;
    }
</style>