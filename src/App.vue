<template>
	<h1>{{ firstName }}</h1>

	<!-- This is using vue directive, this specifies the variable and it's text is imbedded inside -->
	<!-- This works as innerText and replaces the entire content of the html element -->
	<h1 v-text="lastName"></h1>

	<!-- To bind html, text interpolation doesn't work and just renders pure text -->
	<div v-html="htmlBinding"></div>

	<!-- Binding ID to a html element -->
	<p v-bind:id="headingID">Heading</p>

	<!-- Binding Class -->
	<p class="underline" v-bind:class="status">Static Class</p>

	<!-- Dynamic class -->
	<p v-bind:class="warning && 'warning'">Success</p>

	<!-- Conditional class -->
	<p v-bind:class="inStock ? 'success' : 'danger'">
		Conditionally generated class
	</p>

	<!-- Multiple conditional or dynamically generated class -->
	<p
		v-bind:class="[
			inStock && 'success',
			warning && 'underline',
			soldOut && 'danger',
			'placeholder',
		]"
	>
		Dynamically generated multiple class
	</p>

	<!-- Multiple conditional or dynamically generated class using object approach -->
	<p
		v-bind:class="{
			warning: warning,
			'sold-out': soldOut,
		}"
	>
		Dynamically generated multiple class with object approach
	</p>
</template>

<script>
export default {
	name: "App", // Defines the name of the component

	// This contains all the data related to the component
	data() {
		return {
			firstName: "John",
			lastName: "Doe",
			htmlBinding: "<b>Html Binding<b/>",
			headingID: "heading",
			status: "success",
			warning: true,
			inStock: false,
			soldOut: true,
		};
	},
};
</script>

<style>
.underline {
	text-decoration: underline;
}

.success {
	color: mediumseagreen;
}

.danger {
	color: crimson;
}
</style>
