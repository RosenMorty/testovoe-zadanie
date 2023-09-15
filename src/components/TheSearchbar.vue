<template>
    <div class="searchbar-wrapper">
        <div class="searchbar-user">
           Поиск сотрудников
        </div>
        <input class="searchbar-input" placeholder="Введите id или имя">
        <div class="searchbar-result">
            Результаты
        </div>
        <span class="searchbar-result__status">ничего не найдено</span>
        <div

        v-for="itemCard in viewCard"
        :key="itemCard.title"
        >{{ itemCard }}</div>
        <ItemCard
        image="https://www.google.com/url?"
        title="LExa"
        mail="wewe@adsa"
        ></ItemCard>
    </div>
</template>

<script>

import ItemCard from './ItemCard.vue';

    export default {
        name: "ItemCard",
        components: {
                ItemCard
        },

        setup () {
            const viewCard = [{
            image: 'https://www.google.com/url?sa=i&url=https%3A%2F%2Fwww.sima-land.ru%2F667640%2Fkarty-atlasnye-igralnye-36-shtuk%2F&psig=AOvVaw2ueDK8tp_BODMBpYLjM1vO&ust=1694854053693000&source=images&cd=vfe&opi=89978449&ved=0CBAQjRxqFwoTCKCJ5b-drIEDFQAAAAAdAAAAABAE',
            title: 'Karina',
            mail: 'wewe@mail.ru'
            }]
            return {
                viewCard
            }
        }
    }
</script>

<style scoped lang="scss">
    .searchbar {
        &-wrapper {
            margin: 27px 31px 0 20px;
            width: 240px;
            // height: 575px;
            // border-radius: 10px;
            // background: #FDFDFD;
            // box-shadow: 0px 0px 10px 0px rgba(0, 0, 0, 0.10);
            // padding: 27px 0 0 20px;
        }
        &-user {
            color: #333333;
            font-weight: 600;
            font-size: 16px;
            line-height: 22px;
            margin-bottom: 22px;
        }
        &-input {
            box-sizing: border-box;
            width: 100%;
            height: 46px;
            border-radius: 10px;
            padding: 16px;   
            margin-bottom: 22px;
            border: 1.5px solid var(--all-colors-gray-gray-200, #E9ECEF);
            background: var(--all-colors-black-white-white, #FFF);
        }
        &-result {
            color: #333;
            font-family: Montserrat;
            font-size: 16px;
            font-style: normal;
            font-weight: 600;
            line-height: 140%; 
            margin-bottom: 10px;
        }
        &-result__status {
            color: #76787D;
            font-family: Montserrat;
            font-size: 14px;
            font-style: normal;
            font-weight: 400;
            line-height: normal;
        }
    }
</style>

