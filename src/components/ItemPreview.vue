<template>
    <div class="itembar-user">
        <img 
        :src="image"
        alt="ItemPreview"
        class="itembar-image"
        >
            <div class="itembar-text">
            <h1 class="itembar-title">{{ title }}</h1>
            <div class="itembar-email">{{ email }}</div> 
            <div class="itembar-phone">{{ phone }}</div> 
            <div class="itembar-about">{{ about }}</div> 
        </div> 
    </div>
</template>

<script>

export default {
    props: {
        image: String,
        title: String,
        email: String,
        phone: String,
        about: String
    }
}

</script>

<style lang="scss" scoped>
    
</style>