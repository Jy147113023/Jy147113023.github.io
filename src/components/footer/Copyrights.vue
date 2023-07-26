<template>
    <div :style="{color: color, 'font-size': size + 'em'}">
        <p>Copyright ©2023 版权所有 保留一切权利 | </br>
		隐私政策 | 法律声明 |粤X-XXXXXX | </br>
		粤ICP备XXXXXXX号 | 粤公网安备案 </br>
		 XXXXXXXX号 | 中国</p>
    </div>
</template>

<script lang="ts">
    import {Component, Vue} from 'vue-property-decorator';

    @Component({
        props: {
            color: String,
            size: Number,
        },
    })
    export default class Copyrights extends Vue {
    }
</script>
