<script setup>
import CityInfo from './CityInfo.vue';

    defineProps(['citiesData'])
</script>

<template>
    <div class="cities-list">
        <article v-for='(cityInfo,index) in citiesData' :key='index'>
            <CityInfo :cityInfo="cityInfo" />
        </article>
    </div>
</template>
<style scoped>
.cities-list {
    display: flex;
    flex-wrap: wrap;
    gap: 15px;
    justify-content: space-between;
}
</style>