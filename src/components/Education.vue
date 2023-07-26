<template>
    <div class="content education" id="education">
        <ModuleHeader :title="education.header.title" :sub-title="education.header.subtitle"/>
        <div class="AllText">
			<div class="text" id="text" >
				<div class="title">深圳技术大学</div>
				<div class="qualification">本科</div>
				<div class="time">2024届</div>
			</div>
			</br>
			<div class="subject">主修课程：计算机网络、数字电路与逻辑设计、计算机组成原理与系统结构、操作系统、大数据技术原理与应用</div>
			</br>
			<div class="subject">
			目前现任深圳技术大学信息中心项目组软件开发，负责项目核心内容的开发工作，其中参与的自研类项目：大数据与互联网学院心理健康监测管理及辅导一体化平台、心理健康监测系统（二期）、深技大食堂系统、自行采购结果自助发布平台、深技大超市系统、项目申报书查重系统、校长办公室会议系统。
			</div>
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
            education(): Module {
                return this.$store.getters.getModule('education');
            },
        },
    })
    export default class Education extends Vue {
        private loading = true;
    }
</script>

<style scoped lang="scss">
    @import '../styles/variable';
	#text{
		display: flex;
		justify-content: space-between;
	}
	.title {
		display: inline-block;
		text-align: left;
		font-weight: bold;
		font-size: 25px;
	}
	.qualification {
		display: inline-block;
		// margin : 0 0 0 -300px;
		font-weight: bold;
		font-size: 25px;
	}
	.time {
		display: inline-block;
		text-align: right;
		font-weight: bold;
		font-size: 25px;
	}
	.subject {
		font-size: 15px;
		margin : 0 0 0 30px;
	}
</style>