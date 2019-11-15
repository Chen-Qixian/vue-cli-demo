<template>
    <div>
        <div v-if="kk==1">
            111111
        </div>
        <div v-if="kk==2">
            222222
        </div>
        <div v-if="kk==3">
            333333
        </div>
        <div v-if="kk==4">
            444444
        </div>
    </div>
</template>

<script>
    import Msg from './msg.js'
    export default {
        data() {
            return {
                kk: 0
            }
        },
        mounted: function() {
            let _this = this;
            Msg.$on("val", function(m) {
                _this.kk = m;
            })
        }
    }
</script>