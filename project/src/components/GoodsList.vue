<template>
    <div name="show">
        <ul class="goodList">
            <li v-for="good in list" :key="good.key">
                <img :src="good.img">
                <p>{{good.goodName}}</p>
            </li>
        </ul>
    </div>
</template>

<style>
    .goodList li {
        list-style: none;
        width: 200px;
        height: 200px;
        float: left;
        font-size: 9px;
        color: #f40;
        margin-bottom: 30px;
        box-sizing: border-box;
    }
    .goodList img {
        width: 180px;
        height: 180px;
    }
</style>

<script>
    export default {
        name: "show",
        data() {
            let url = "";
            if(this.goodId == 1) {
                url="json/laptop.json";
            }
            else if(this.goodId == 2) {
                url = "json/cellphone.json";
            }
            else {
                url="json/laptop.json";
            }
            this.$http.get(url).then((res) => {
                this.list = res.data;
            })
            return {
                list: []
            }
        },
        props: {
            goodId: {
                type: Number,
                required: true
            }
        },
        watch: {
            goodId() {
                let url = "";
                if(this.goodId == 1) {
                    url="json/laptop.json";
                }
                else if(this.goodId == 2) {
                    url = "json/cellphone.json";
                }
                else {
                    url="json/laptop.json";
                }
                this.$http.get(url).then((res) => {
                    this.list = res.data;
                })
                return {
                    list: []
                }
            }
        }
    }
</script>