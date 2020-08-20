<template>
  <div v-bind="$attrs" @click="sentHome" style="width:100px;height:100px;border:1px solid red">sdsadsad</div>
</template>

<script>
export default {
	created () {
		console.log('c组件接收值')
		console.log(this.$attrs)
	},
	methods: {
		sentHome () {
			this.$emit('test1', 'c组件')
		}
	}
}
</script>

<style>

</style>