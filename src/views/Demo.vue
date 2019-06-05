<template>
	<div>
		<hello-world ></hello-world>
	</div>
</template>

<script>
// import HelloWorld from ''
export default{
	components:{HelloWorld},
	props:{
		path: String,
	},
	data() {
		return {
			name: "Hello"
		}
	},
	methods: {
		getList: function(){

		}
	}
}
</script>