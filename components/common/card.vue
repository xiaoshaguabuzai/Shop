<!-- 基础卡片组件 -->
<template>
	<view class="card">
		<!-- head -->
		<view v-if="showhead" class="p-2 border-bottom main-border-color">
			<slot name="title">
				<text v-if="headTitle" class="font-md font-weight">{{headTitle}}</text>
			</slot>
		</view>
		<!-- body -->
		<view class="">
			<image v-if="bodyCover" :src="bodyCover" mode="widthFix"/>
			<slot/>
			</view>
	</view>
</template>

<script>
	export default{
		props:{
			//头部标题
			headTitle:String,
			//封面图
			bodyCover:String,
			//是否显示头部
			showhead:{
				type:Boolean,
				default:true
			}
			
		}
	}
</script>

<style>
</style>
