
<template>
    <main>
        <div class="searchbar-wrapper">
        <div class="searchbar-user">
            Поиск сотрудников
        </div>
        <!-- <input class="searchbar-input" placeholder="Введите id или имя"> -->
        <search-u>
            
        </search-u>
        <div class="searchbar-result">
            Результаты
        </div>
        <item-card v-for="selected of selectedUser.selected"
        :key="selected.id"
        :selected="selected"
        >
        {{ selectedUser.selected }}
        </item-card>
        </div>
    </main>
</template>

<script setup>

import SearchU from './SearchU.vue';
import ItemCard from './ItemCard.vue';
import { useSelectedUserStore } from '../store/SelectedUser'

const selectedUser = useSelectedUserStore()

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
        margin-bottom: 29px;
        border: 1.5px solid var(--all-colors-gray-gray-200, #E9ECEF);
        background: var(--all-colors-black-white-white, #FFF);
        color: #76787D;
        padding: 16px 24px;
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

