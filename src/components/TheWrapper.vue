<template>
    <div class="the-wrapper">

        <TheToolbar></TheToolbar>
        <div class="wrapper-container">
            <TheSearchbar>

            </TheSearchbar>
            <div class="wrapper-divider">

            </div>
            <TheResult>
                <ItemPreview>
                    
                </ItemPreview>
            </TheResult>
        </div>
        <slot>
            
        </slot>
    </div>
</template>

<script>
import TheToolbar from './TheToolbar.vue';
import TheSearchbar from './TheSearchbar.vue';
import TheResult from './TheResult.vue'
import ItemPreview from './ItemPreview.vue';


export default {
    name: 'App',
    components: {
        TheToolbar,
        TheSearchbar,
        TheResult,
        ItemPreview
    }
}
</script>

<style scoped lang="scss">
    .the-wrapper {
        margin: 0 50px 0 50px;
    }
    .wrapper {
        &-container {
            display: flex;
            height: 575px;
            border-radius: 10px;
            background: #FDFDFD;
            box-shadow: 0px 0px 10px 0px rgba(0, 0, 0, 0.10);
            }   
        &-divider {
            width: 1px;
            height: 100%;
            background-color: #E0E0E0;
        }
    }
</style>