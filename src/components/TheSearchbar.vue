
<template>
    <div class="searchbar-wrapper">
        <div class="searchbar-user">
            Поиск сотрудников
        </div>
        <input class="searchbar-input" placeholder="Введите id или имя">
        <div class="searchbar-result">
            Результаты
        </div>
        <span v-if="viewCard < 1" class="searchbar-result__status">ничего не найдено</span>
        <div 
            v-for="(itemCard, index) in viewCard" 
            :key="index">
                <ItemCard 
                    :image="itemCard.image" 
                    :title="itemCard.title" 
                    :email="itemCard.email"
                ></ItemCard>
        </div>
    </div>
</template>

<script>

import ItemCard from './ItemCard.vue';

export default {
    components: {
        ItemCard
    },
    data() {
        return {
            viewCard: [
                {
                    image: 'data:image/jpeg;base64,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',
                    title: 'Bret',
                    email: 'Sincere@april.biz'
                },
                {
                    image: 'data:image/jpeg;base64,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',
                    title: 'Vlad',
                    email: 'rolit0852@gmail.com'
                }
            ]
        }
    }
}
</script>

<style scoped lang="scss">
.searchbar {
    &-wrapper {
        margin: 27px 31px 0 20px;
        width: 240px;
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

