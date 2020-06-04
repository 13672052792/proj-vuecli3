<template>
    <div name="show">
        <ul class="goodlist">
            <li v-for="goods in list">
                <img v-bind:src="goods.img">
                <p>{{goods.goodname}}</p>
            </li>
        </ul>
    </div>
</template>

<style>
    .goodlist li {
        list-style: none;
        float: left;
        font-size: 9px;
        color: red;
        margin-bottom: 20px;
        margin-left: 10px;
    }
</style>

<script>
    export default {
        name: "show",
        data() {
            var _this = this;
            var url = ""
            if (_this.goodid == 1) {
                url = 'json/tp.json'
            } else if (_this.goodid == 2) {
                url = 'json/bj.json'
            } else {
                url = 'json/tp.json'
            }
            this.$http.get(url).then(function (res) {
                _this.list = res.data;
            })
            return {
                list: []
            }
        },
        props: {
            goodid: Number
        },
        watch: {
            goodid() {
                var _this = this;
                var url = "";
                if (_this.goodid == 1) {
                    url = 'json/tp.json'
                } else if (_this.goodid == 2) {
                    url = 'json/bj.json'
                } else {
                    url = 'json/tp.json'
                }
                this.$http.get(url).then(function (res) {
                    _this.list = res.data;
                })
                return {
                    list: []
                }
            }
        },
    }

</script>