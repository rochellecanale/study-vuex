<template>
	<div>
		<h1>User List</h1>
		<p>{{ title }}</p>
		<button @click="increment()">Test</button>
	</div>
</template>
<script>

import UserStore from '../store/users.js';

export default {
	name: 'UserList',
	store: UserStore,
	data() {
		return {
			title: 'test'
		}
	},
	methods: {
		increment: function() {
			this.$store.commit('increment');
			console.log(this.$store.state.count);
		}
	}
}
</script>
<style scoped>
	h1, p {
		text-align: left;
	}
</style>