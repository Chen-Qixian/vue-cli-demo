<template>
    <div>
        <p>This is Page A.</p>
        <p><router-link to="/">Back</router-link></p>
        <p><router-link to="/a1">Goto A1</router-link></p>
        <!-- 使用子路由：可以使父路由页面内容保留，子路由内容显示 -->
        <router-view></router-view>
    </div>
</template>

<script>
export default {
    
}
</script>

<style>

</style>