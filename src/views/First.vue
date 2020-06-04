<template lang="">
    <div class="main">
        <div class="left">
            <Left></Left>
        </div>
        <div class="right">
            <div class="top">
                <img src="img/01.jpg">

            </div>
            <div class="bottom">
                <Right></Right>
            </div>
        </div>
    </div>
</template>

<script>
    import Left from '../components/Left.vue'
    import Right from '../components/Right.vue'

    export default {
        components: {
            Left,
            Right
        }
    }

</script>

<style>
    * {
        padding: 0;
        margin: 0;
    }
    
    .main {
        width: 100%;
        height: 800px;
        margin: 20px auto;
        /*background-color: red;*/
    }
    
    .left {
        width: 15%;
        float: left;
        margin-right: 10px;
        margin-left: 20px;
    }
    
    .right {
        width: 70%;
        float: left;
        margin-left: 10px;
    }
    
    .top img {}

    .left,.right{
        background-color: #f5f5f5;
    }
</style>