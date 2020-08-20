<template>
 	<div>
		<!-- <div style="">{{ toB }}</div> -->
  	<div style="width:200px;height:200px;border:1px solid blue" @click="setB">
		</div>
		<C v-bind="$attrs" v-on="$listeners"/>
	</div>
  
</template>

<script>
import C from './c'
export default {
	components: {
		C
	},
	props: {
		toB: {
			type: String,
			default: ''
		},
		toC: {
			type: String,
			default: ''
		}
	},
	created () {
		console.log('b组件接收值')
		console.log(this.$attrs)
	},
	methods: {
		setB() {
			this.$emit('test2', 'B组件')
		}
	}
}
</script>

<style>

</style>