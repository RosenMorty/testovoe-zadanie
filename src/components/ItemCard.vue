<template>
    <div class="cardbar-user">
        <img 
        :src="image"
        alt="ItemCard"
        class="cardbar-image"
        >
        <div class="cardbar-text">
            <h1 class="cardbar-title">{{ title }}</h1>
            <div class="cardbar-email">{{ email }}</div> 
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
    .cardbar {
        &-text {
            margin: 15px 0 18px 15px;
        }
        &-user:hover {
            background-color: #E0E0E0;
        }
        &-user {
            width: 240px;
            height: 70px;
            border-radius: 10px;
            overflow: hidden;
            background: #FFF;
            box-shadow: 0px 0px 10px 0px rgba(0, 0, 0, 0.10);
            display: flex;
            box-sizing:border-box;
            margin-bottom: 18px;
        }
        &-image {
            width: 70px;
            height: 70px;
            border-right: 1px solid #E0E0E0;
        }
        &-title {
            width: 115px;
            height: 15px;
            color: #333;
            font-family: Montserrat;
            font-size: 14px;
            font-style: normal;
            font-weight: 600;
            line-height: normal;
            margin-bottom: 5px;
        }
        &-email {
            color: #76787D;
            font-family: Montserrat;
            font-size: 14px;
            font-style: normal;
            font-weight: 400;
            line-height: normal;
        }
    }
</style>