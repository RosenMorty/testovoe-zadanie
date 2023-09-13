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
    </div>
</template>

<style scoped lang="scss">
    .searchbar {
        &-wrapper {
            width: 291px;
            height: 575px;
            border-radius: 10px;
            background: #FDFDFD;
            box-shadow: 0px 0px 10px 0px rgba(0, 0, 0, 0.10);
            padding: 27px 0 0 20px;
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
            width: 240px;
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

