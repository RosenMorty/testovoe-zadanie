<template>
    <form @submit.prevent="selectedUser.getUsers(whereUser)">
        <input 
            type="text" 
            class="searchbar-input" 
            placeholder="Введите id или имя" 
            v-model="whereUser">
    </form>
</template>

<script setup>

import { ref } from 'vue';
import { useSelectedUserStore } from '../store/SelectedUser'
const selectedUser = useSelectedUserStore()
const whereUser = ref("")

</script>

<style scoped lang="scss">

.searchbar{
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
}

</style>