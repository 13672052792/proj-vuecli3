<template lang="">
    <div>
        <div class="title">热门推荐</div>
        <ul class="menu">
            <li @click="menu1">图片</li>
            <li @click="menu2">背景</li>
            <li @click="menu3">图片</li>
            <li @click="menu4">背景</li>
            <li>图片</li>
            <li>背景</li>
            <li>图片</li>
            <li>背景</li>
            <li>图片</li>
            <li>背景</li>
            <li>图片</li>
            <li>背景</li>
        </ul>
    </div>
</template>

<script>
    import Msg from './Msg.js'

    export default {
        methods:{
            menu1:function(){
                Msg.$emit("val","1");
            },
            menu2:function(){
                Msg.$emit("val","2");
            },
            menu3:function(){
                Msg.$emit("val","3");
            },
            menu4:function(){
                Msg.$emit("val","4");
            }
        }
    }

</script>

<style>
    .title {
        width: 100px;
        color: red;
    }
    
    .menu li {
        list-style: none;
        height: 50px;
        margin-bottom: 3px;
        background-color: white;
        line-height: 50px;
        cursor: pointer;
    }
</style>