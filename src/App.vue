<template>
  <div>
	<h1>Witaj w systemie do zapisów na zajęcia</h1>
	<h2 v-if="logged == true">Witaj {{ email }}!</h2>
	<div v-if="logged == false">
		Zaloguj się e-mailem
		<input type="email" v-model="email">
		<button @click="enter()">Wchodzę</button>
	</div>
  </div>
</template>

<script>
import "milligram";

export default {
	data() {
		return {
			email: '',
			password: '',
			logged: false
		};
	},
	methods: {
		enter() {
			this.logged = true
		}
	}
}
</script>

<style>

</style>
