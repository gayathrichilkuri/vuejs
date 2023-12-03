<script setup>
    defineProps(['cityInfo'])
</script>

<template>
    <div class="card">
        <h2>{{ cityInfo.city }}</h2>
        <ul>
            <li>State: {{ cityInfo.state }}</li>
            <li>Country: {{ cityInfo.country }}</li>
            <li>Population: {{ cityInfo.population }}</li>
            <li>Density: {{ cityInfo.density }}</li>
            <li>Area: {{ cityInfo.area }}</li>
            <li>TimeZone: {{ cityInfo.timezone }}</li>
            
        </ul>
    </div>
</template>

<style scoped>
.card {
    padding: 15px;
    background-color: #d4440d;
    color: #fff;
    width: 350px;

}
h2 {
    font-size: 28px;
    font-weight: bold;
    margin-bottom: 10px;
}
h2::after{
    background-color: #fff;
    content: "";
    display: block;
    height: 1px;
    margin: 15px 0 10px;
    width: 100%;
}
ul {
    color: #fff;
    list-style-position: inside;
    margin: 0;
    padding-left: 0;
}
li{
    font-size: 19px;
    font-weight: bold;
    color: #fff;
    letter-spacing: .1px;
    margin: 5px 0;
    padding: 5px 0 5px 30px;
}
li:nth-child(2n) {
    background: #ef6f0a;
}
</style>