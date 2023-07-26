<template>
    <div class="content hobbies" id="hobbies">
        <ModuleHeader :title="hobbies.header.title" :sub-title="hobbies.header.subtitle"/>
        &emsp;&emsp;<div class="AllText">
			作为一名程序员，我非常喜欢面对各种挑战并解决问题。我认为在编写代码时，每一个细节都非常重要，因此我非常注重代码的质量和可维护性。所以在对知识的探索时期，我通过不断学习新技术和参与开源项目来提高自己的技能。
			同时，我的兴趣爱好也很广泛。我热衷于打羽毛球，这项运动让我身体健康、增强协调能力。此外，我也很喜欢听音乐，无论是工作中还是闲暇时间，流行音乐、古典音乐、电子音乐等都是我经常聆听的类型。我认为音乐可以让人放松身心，帮助我更好地集中精力完成工作。
		</div>
		
	</div>
</template>

<script lang="ts">
    import {Component, Vue} from 'vue-property-decorator';
    import ModuleHeader from '@/components/module/ModuleHeader.vue';
    import ModuleSkeleton from '@/components/module/ModuleSkeleton.vue';
    import {Module} from '@/api/user_interface';

    @Component({
        components: {
            ModuleHeader,
            ModuleSkeleton,
        },
        computed: {
            hobbies(): Module {
                return this.$store.getters.getModule('hobbies');
            },
        },
    })
    export default class Education extends Vue {
        private loading = true;
    }
</script>

<style scoped lang="scss">
    @import '../styles/variable';
	.AllText {
		font-size: 15px;
		margin : 0 0 30px 30px;
	}
	.AllText::before {
	    content: "\00a0\00a0\00a0\00a0\00a0\00a0\00a0"; 
	  }
</style>