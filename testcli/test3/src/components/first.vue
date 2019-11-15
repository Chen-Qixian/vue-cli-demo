<template>
    <div>
        <router-link class="style1" to="/a">Link to A </router-link>
        <router-link class="style1" to="/b">Link to B</router-link>
        <router-view></router-view>
    </div>
</template>

<style>
    @import "../../public/style.css";
    /* a {
        color: red;
    } */
    /* .style1 {
        color: blue;
        font-size: 20px;
    } */
</style>