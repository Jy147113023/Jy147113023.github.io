<template>
    <div>
        <img alt="技能条" src="../../assets/skill.png"/>
    </div>
</template>

<script lang="ts">
    import {Component, Vue} from 'vue-property-decorator';

    @Component({})
    export default class Badge extends Vue {
    }
</script>

<style scoped lang="scss">
    a {
        margin: 0.5em;
    }
</style>
