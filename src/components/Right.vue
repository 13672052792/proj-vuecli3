<template lang="">
    <div>
        <div v-if="kk==1">
            <GoodList :goodid="1"></GoodList>
        </div>
        <div v-else-if="kk==2">
            <GoodList :goodid="2"></GoodList>
        </div>
        <div v-else-if="kk==3">
            33333333
        </div>
        <div v-else-if="kk==4">
            44444444
        </div>
        <div v-else>
            <GoodList :goodid="0"></GoodList>
        </div>
    </div>
</template>

<script>
    import Msg from './Msg.js'
    import GoodList from './goodsList.vue'

    export default {
        data(){
            return{
                kk:"0"
            }
        },
        mounted() {
            var _this = this
            Msg.$on('val',function(m){
                _this.kk = m;
            }) 
        },
        components:{
            GoodList
        }
    }

</script>