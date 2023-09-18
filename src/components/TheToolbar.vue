<template>
    <div class="toolbar-wrapper">
        <div class="toolbar-logo">
            Жилфонд
        </div>
        <div class="toolbar-user">
            Пользователь
        </div>
    </div>
</template>

<style scoped lang="scss">
.toolbar {
    &-wrapper {
        display: flex;
        justify-content: space-between;
        height: 115px;
        align-items: center;
    } 
    
    &-logo {
        color: #E31F24;
        font-weight: 700;
        font-size: 32px;
        line-height: 39px;
}
    &-user {
        color: #333;
        font-family: Montserrat;
        font-size: 16px;
        font-style: normal;
        font-weight: 400;
        line-height: normal;
}

    
}
</style>